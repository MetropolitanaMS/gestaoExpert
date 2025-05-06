<template>
  <div
    class="flex w-full overflow-hidden bg-secondary bg-[url('/assets/shape/10.png')] bg-no-repeat py-37"
  >
    <div
      class="flex flex-col lg:flex-row items-center justify-center px-4 lg:px-20 mx-4 lg:mx-20 w-full"
    >
      <div
        class="flex flex-col w-full lg:w-2/5 px-3.5 items-center justify-center"
      >
        <h2 class="text-3xl text-white text-center leading-12 font-bold mb-3.5">
          Seja um parceiro do <br />
          Gestão Expert
        </h2>
        <p class="text-sm text-white text-center leading-7">
          Amplie seu portfólio e ofereça soluções inovadoras para a gestão
          pública. Junte-se à nossa rede de parceiros e faça parte dessa
          transformação.
        </p>
      </div>

      <div
        class="flex items-center justify-center m-10 w-full md:w-3/5 overflow-hidden relative"
      >
        <div class="whitespace-nowrap animate-scroll flex">
          <div
            v-for="client in [...clients, ...clients]"
            :key="client.id + '-' + Math.random()"
            class="flex items-center justify-center mx-6 shrink-0"
          >
            <NuxtImg class="w-[150px] h-[80px]" :src="client.image" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionClients",
  data() {
    return {
      clients: [
        {
          image: "./assets/logos/v2TEC.png",
          alt: "logo da v2 TEC",
        },
        {
          image: "/assets/logos/ArcGIS.png",
          alt: "logo da ArcGIS",
        },
        {
          image: "/assets/logos/Betha.png",
          alt: "logo da Betha",
        },
        {
          image: "/assets/logos/Toccato.png",
          alt: "logo da Toccato",
        },
      ],
      currentIndex: 0,
      interval: null,
    };
  },
  computed: {
    visibleClients() {
      return [...this.clients, ...this.clients];
    },
  },
  mounted() {
    this.interval = setInterval(() => {
      this.currentIndex = (this.currentIndex + 1) % this.clients.length;
    }, 10);
  },
  beforeUnmount() {
    clearInterval(this.interval);
  },
};
</script>

<style scoped>
@keyframes scroll {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-scroll {
  animation: scroll 20s linear infinite;
}
</style>
