<template>
  <section
    class="w-full bg-gray bg-[url('/assets/shape/1.svg')] bg-contain bg-no-repeat bg-bottom pt-20 relative"
    id="features"
  >
    <div
      class="px-3.5 flex flex-col justify-center items-center gap-8 text-center"
    >
      <h2 class="font-bold text-3xl">Módulos & Funcionalidades</h2>
      <div class="w-full max-w-[70px] flex justify-between gap-1">
        <div class="h-0.5 w-1/6 bg-primary rounded-full"></div>
        <div class="h-0.5 w-full bg-primary rounded-full"></div>
      </div>
      <p class="text-black-paragraph">
        Módulos do Gestão Expert para uma Gestão Completa e Eficiênte.
      </p>
    </div>
    <div class="relative">
      <HexMenuItem
        v-for="(slide, index) in slides"
        @click="setSlide(index)"
        :key="index"
        :label="slide.label"
        color="#1e2a38"
        hoverColor="#2c3150"
        :isSelected="index === currentIndex"
        :selectedColor="'#2c3150'"
        class="rotate-90 w-[10vw] h-[11.8vw] min-[2000px]:w-[9vw] min-[2000px]:h-[10.8vw] min-[4000px]:w-[8vw] min-[4000px]:h-[9.8vw] absolute"
        :class="
          index === currentIndex ? 'focus:ring focus:ring-violet-300' : ''
        "
        :style="
          positionsWithSix[index]
            ? {
                left: positionsWithSix[index].left,
                top: positionsWithSix[index].top,
              }
            : {}
        "
      />
    </div>
    <div
      class="overflow-hidden relative w-full mt-[20%] lg:mt-[18%]"
      @touchstart="onTouchStart"
      @touchmove="onTouchMove"
      @touchend="onTouchEnd"
    >
      <div
        class="flex transition-transform duration-700 ease-[cubic-bezier(0.6, 0, 0.2, 1)]"
        :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
      >
        <div
          v-for="(slide, index) in slides"
          :key="index"
          class="flex flex-col lg:flex-row w-full flex-shrink-0 items-center justify-center min-h-[250px] lg:min-h-[440px]"
        >
          <svg
            v-if="screenWidth >= 1024"
            :class="[
              currentIndex === 0 ? 'text-gray-300' : 'text-gray-600',
              'text-solid h-10 w-10 hover:cursor-pointer mx-2',
            ]"
            @click="prevSlide"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 256 512"
          >
            <path
              fill="currentColor"
              d="M192 448c-8.188 0-16.38-3.125-22.62-9.375l-160-160c-12.5-12.5-12.5-32.75 0-45.25l160-160c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25L77.25 256l137.4 137.4c12.5 12.5 12.5 32.75 0 45.25C208.4 444.9 200.2 448 192 448z"
            />
          </svg>
          <div
            class="bg-white shadow-lg w-full max-w-[640px] lg:max-w-[350px] h-auto min-h-[250px] lg:h-[440px] p-8 lg:m-5 flex flex-col order-2 lg:order-1"
          >
            <div class="flex justify-between items-start">
              <h2 class="my-2 text-2xl font-bold text-[#333]">
                {{ slide.title }}
              </h2>
              <h1 class="text-gray-300 text-4xl font-bold">
                {{ (index + 1).toString().padStart(2, "0") }}
              </h1>
            </div>
            <p class="text-base text-black-paragraph mt-4">
              {{ slide.description }}
            </p>

            <div class="flex-grow"></div>

            <button
              type="button"
              class="mt-4 ml-auto rounded-full shadow-lg p-2 bg-gray-200 transition duration-200 hover:shadow-2xl hover:scale-120 cursor-pointer"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-6 h-6 text-black"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 5l7 7-7 7"
                />
              </svg>
            </button>
          </div>

          <div
            class="h-auto min-h-[250px] lg:h-[440px] shadow-lg flex lg:p-3.5 lg:m-5 bg-white order-1 lg:order-2"
          >
            <NuxtImg
              class="w-full h-full max-h-[400px] object-contain"
              :src="slide.image"
              :alt="slide.alt"
            />
          </div>
          <svg
            v-if="screenWidth >= 1024"
            :class="[
              currentIndex === slides.length - 1
                ? 'text-gray-300'
                : 'text-gray-600',
              'text-bold h-10 w-10 hover:cursor-pointer mx-2 order-3',
            ]"
            @click="nextSlide"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 256 512"
          >
            <path
              fill="currentColor"
              d="M64 448c-8.188 0-16.38-3.125-22.62-9.375c-12.5-12.5-12.5-32.75 0-45.25L178.8 256L41.38 118.6c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0l160 160c12.5 12.5 12.5 32.75 0 45.25l-160 160C80.38 444.9 72.19 448 64 448z"
            />
          </svg>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { ArrowRight } from "lucide-vue-next";

export default {
  name: "SectionFeatures",
  data() {
    return {
      slides: [
        {
          id: 0,
          image: "./assets/dashboard/1.png",
          alt: "Mapa estratégico.",
          label: "Mapa estratégico",
          title: "Mapa Estratégico",
          description:
            "Mapas, Objetivos, Indicadores. Esté módulo foca no planejamento estratégico, permitindo a visualização de objetivos e indicadores de desempenho",
        },
        {
          id: 1,
          image: "./assets/dashboard/2.png",
          alt: "Ações, projetos e iniciativas.",
          label: "Ações, Projetos e Iniciativas",
          title: "Ações, projetos e iniciativas",
          description:
            "Escopo, Cronograma, Financeiro, Riscos. Gerenciamento de projetos e ações, incluindo planejamento, orçamento e análise de riscos.",
        },
        {
          id: 2,
          image: "./assets/dashboard/3.png",
          alt: "Processos.",
          label: "Processos",
          title: "Processos",
          description:
            "Documentação de processos. Mapeamento e documentação dos processos internos.",
        },
        {
          id: 3,
          image: "./assets/dashboard/4.png",
          alt: "Integrações.",
          label: "Integrações",
          title: "Integrações",
          description:
            "Banco de dados, APIs, Arquivos de integração com outras plataformas e banco de dados, permitindo a centralização de informações.",
        },
        {
          id: 4,
          image: "./assets/dashboard/5.png",
          alt: "Relatórios/BI.",
          label: "Relatórios/BI",
          title: "Relatórios/BI",
          description:
            "Dashboards, Relatórios, Exportação de dados. Geração de relatórios e dashboards para acompanhamento do desempenho e Business Intelligence.",
        },
        {
          id: 5,
          image: "./assets/dashboard/6.png",
          alt: "Demais módulos.",
          label: "Demais módulos",
          title: "Demais módulos",
          description:
            "Matriz de Swot, 5W2h, Agenda, Auditoria, Plano de compras anual, ODS. Funcionalidades adicionais, incluindo ferramentas de análise estratégica (Matriz SWOT, 5W2H), agenda, auditoria, planejamento de compras e acompanhamento dos Objetivos de Desenvolvimento Sustentável(ODS).",
        },
      ],
      currentIndex: 0,
      positionsWithTwo: [
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
      ],
      positionsWithThree: [
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
      ],
      positionsWithFour: [
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
      ],
      positionsWithFive: [
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
        { left: "54.7vw", top: "0vw" },
      ],
      positionsWithSix: [
        { left: "28.3vw", top: "0vw" },
        { left: "32.7vw", top: "7.6vw" },
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
      ],
      positionsWithSeven: [
        { left: "28.3vw", top: "0vw" },
        { left: "32.7vw", top: "7.6vw" },
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
        { left: "54.7vw", top: "0vw" },
      ],
      positionsWithEight: [
        { left: "28.3vw", top: "0vw" },
        { left: "32.7vw", top: "7.6vw" },
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
        { left: "54.7vw", top: "0vw" },
        { left: "59.1vw", top: "7.6vw" },
      ],
      positionsWithNine: [
        { left: "28.3vw", top: "0vw" },
        { left: "32.7vw", top: "7.6vw" },
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
        { left: "54.7vw", top: "0vw" },
        { left: "59.1vw", top: "7.6vw" },
        { left: "63.5vw", top: "0vw" },
      ],
      positionsWithTen: [
        { left: "19.5vw", top: "0vw" },
        { left: "23.9vw", top: "7.6vw" },
        { left: "28.3vw", top: "0vw" },
        { left: "32.7vw", top: "7.6vw" },
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
        { left: "54.7vw", top: "0vw" },
        { left: "59.1vw", top: "7.6vw" },
      ],
      positionsWithEleven: [
        { left: "19.5vw", top: "0vw" },
        { left: "23.9vw", top: "7.6vw" },
        { left: "28.3vw", top: "0vw" },
        { left: "32.7vw", top: "7.6vw" },
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
        { left: "54.7vw", top: "0vw" },
        { left: "59.1vw", top: "7.6vw" },
        { left: "63.5vw", top: "0vw" },
      ],
      positionsWithTwelve: [
        { left: "19.5vw", top: "0vw" },
        { left: "23.9vw", top: "7.6vw" },
        { left: "28.3vw", top: "0vw" },
        { left: "32.7vw", top: "7.6vw" },
        { left: "37.1vw", top: "0vw" },
        { left: "41.5vw", top: "7.6vw" },
        { left: "45.9vw", top: "0vw" },
        { left: "50.3vw", top: "7.6vw" },
        { left: "54.7vw", top: "0vw" },
        { left: "59.1vw", top: "7.6vw" },
        { left: "63.5vw", top: "0vw" },
        { left: "67.8vw", top: "7.6vw" },
      ],
      // firstLine: [
      //   { left: "20vw", top: "0vw" },
      //   { left: "32vw", top: "0vw" },
      //   { left: "44vw", top: "0vw" },
      //   { left: "56vw", top: "0vw" },
      //   { left: "68vw", top: "0vw" },
      // ],
      // secondLine: [
      //   { left: "26vw", top: "10.3vw" },
      //   { left: "38vw", top: "10.3vw" },
      //   { left: "50vw", top: "10.3vw" },
      //   { left: "62vw", top: "10.3vw" },
      // ],
      // thirdLine: [
      //   { left: "20vw", top: "20.3vw" },
      //   { left: "32vw", top: "20.3vw" },
      //   { left: "44vw", top: "20.3vw" },
      //   { left: "56vw", top: "20.3vw" },
      //   { left: "68vw", top: "20.3vw" },
      // ],
      startX: 0,
      endX: 0,
      screenWidth: window.innerWidth,
    };
  },
  methods: {
    nextSlide() {
      if (this.currentIndex < this.slides.length - 1) {
        this.currentIndex++;
      }
    },
    prevSlide() {
      if (this.currentIndex > 0) {
        this.currentIndex--;
      }
    },
    setSlide(index) {
      this.currentIndex = index;
    },

    onTouchStart(event) {
      this.startX = event.touches[0].clientX;
    },
    onTouchMove(event) {
      this.endX = event.touches[0].clientX;
    },
    onTouchEnd() {
      const deltaX = this.startX - this.endX;
      if (deltaX > 50) this.nextSlide();
      else if (deltaX < -50) this.prevSlide();
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
