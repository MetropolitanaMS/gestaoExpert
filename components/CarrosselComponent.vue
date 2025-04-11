<template>
  <div
    v-if="screenWidth < 1024"
    class="relative overflow-hidden w-full max-w-[600px] mx-auto lg:hidden"
  >
    <div
      class="flex transition-transform duration-300 ease-in-out"
      :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
      @touchstart="onTouchStart"
      @touchmove="onTouchMove"
      @touchend="onTouchEnd"
    >
      <div
        v-for="(slide, index) in slides"
        :key="index"
        class="min-w-full text-center flex flex-col justify-center items-center gap-3"
      >
        <div class="relative">
          <NuxtImg
            :src="slide.image"
            :alt="slide.alt"
            class="w-[60px] h-[60px] text-primary"
          />
        </div>
        <h2 class="my-2 text-xl font-bold text-[#333]">{{ slide.title }}</h2>
        <p class="text-base text-[#666]">{{ slide.text }}</p>
      </div>
    </div>
    <div class="flex justify-center mt-20">
      <span
        v-for="(slide, index) in slides"
        :key="index"
        class="w-5 h-5 mx-1 bg-white rounded-full cursor-pointer border-2 border-[#e7e7e7] flex justify-center items-center"
        @click="currentIndex = index"
      >
        <span
          v-if="currentIndex === index"
          class="w-2 h-2 bg-light-blue rounded-full"
        ></span>
      </span>
    </div>
  </div>
  <div
    v-if="screenWidth >= 1024"
    class="w-full flex justify-center items-center"
  >
    <div
      class="max-w-[960px] min-[1200px]:max-w-[1400px] flex justify-center items-start gap-8 px-12"
    >
      <div
        v-for="(slide, index) in slides"
        :key="index"
        class="w-fit text-start flex flex-col justify-center items-start gap-3"
      >
        <div class="w-fit relative">
          <NuxtImg
            :src="slide.image"
            :alt="slide.alt"
            class="w-[60px] h-[60px] text-primary"
          />
        </div>
        <h2 class="my-2 text-xl font-bold text-[#333]">{{ slide.title }}</h2>
        <p class="text-base text-[#666]">{{ slide.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CarrosselComponent",
  data() {
    return {
      slides: [
        {
          image: "/assets/icons/drag.svg",
          alt: "Ícone de uma mão tocando numa tela",
          title: "Eficiência para Governança Pública",
          text: "Otimize processos e entregue mais resultados com os mesmos recursos. Ênfase na otimização e melhor aproveitamento dos recursos.",
        },
        {
          image: "/assets/icons/website.svg",
          alt: "Ícone de um monitor em um website com segurança",
          title: "Rastreabilidade e Transparência",
          text: "Atenda às exigências legais e aos princípios de transparência, monitorando cada etapa com clareza. Foco no cumprimento legal e na transparência dos processos.",
        },
        {
          image: "/assets/icons/integration.svg",
          alt: "Ícone de um monitor com cubos interligados",
          title: "Alinhamento com Políticas Públicas",
          text: "Assegure que ações e projetos estejam alinhados aos planos institucionais e às metas governamentais. Garantia de alinhamento estratégico entre ações, projetos e metas.",
        },
        {
          image: "/assets/icons/rgb.svg",
          alt: "Ícone de um diagrama de vern com 3 circulos parcialmente se sobrepondo",
          title: "Gestão com Comunicação Integrada",
          text: "Compartilhe informações, centralize documentos e otimize o fluxo de trabalho entre diferentes departamentos, promovendo uma gestão mais integrada e transparente.",
        },
      ],
      currentIndex: 0,
      startX: 0,
      endX: 0,
      screenWidth: window.innerWidth,
    };
  },
  methods: {
    onTouchStart(event) {
      this.startX = event.touches[0].clientX;
    },
    onTouchMove(event) {
      this.endX = event.touches[0].clientX;
    },
    onTouchEnd() {
      const deltaX = this.startX - this.endX;
      if (deltaX > 50 && this.currentIndex < this.slides.length - 1) {
        this.currentIndex++;
      } else if (deltaX < -50 && this.currentIndex > 0) {
        this.currentIndex--;
      }
    },
    updateScreenWidth() {
      this.screenWidth = window.innerWidth;
    },
  },
  mounted() {
    this.updateScreenWidth();
    window.addEventListener("resize", this.updateScreenWidth);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.updateScreenWidth);
  },
};
</script>
