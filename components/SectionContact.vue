<template>
  <div class="py-28 relative">
    <div class="flex lg:flex-row mx-28 px-3.5">
      <div class="flex flex-col items-center px-3.5">
        <div
          class="flex flex-col items-center rounded-md bg-secondary w-5/5 p-13 mr-5"
        >
          <div class="mb-6">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              fill="currentColor"
              class="w-17 h-17 text-white"
            >
              <path
                d="M280 0C408.1 0 512 103.9 512 232c0 13.3-10.7 24-24 24s-24-10.7-24-24c0-101.6-82.4-184-184-184c-13.3 0-24-10.7-24-24s10.7-24 24-24zm8 192a32 32 0 1 1 0 64 32 32 0 1 1 0-64zm-32-72c0-13.3 10.7-24 24-24c75.1 0 136 60.9 136 136c0 13.3-10.7 24-24 24s-24-10.7-24-24c0-48.6-39.4-88-88-88c-13.3 0-24-10.7-24-24zM117.5 1.4c19.4-5.3 39.7 4.6 47.4 23.2l40 96c6.8 16.3 2.1 35.2-11.6 46.3L144 207.3c33.3 70.4 90.3 127.4 160.7 160.7L345 318.7c11.2-13.7 30-18.4 46.3-11.6l96 40c18.6 7.7 28.5 28 23.2 47.4l-24 88C481.8 499.9 466 512 448 512C200.6 512 0 311.4 0 64C0 46 12.1 30.2 29.5 25.4l88-24z"
              />
            </svg>
          </div>
          <p class="text-center text-white text-sm mb-4 leading-8">
            Quer ser nosso parceiro? Entre em contato agora mesmo! Oferecemos
            suporte completo e oportunidades de crescimento conjunto.
          </p>
          <button
            type="button"
            class="w-full p-1.5 rounded-sm text-primary font-bold bg-white mt-7"
          >
            ENTRAR EM CONTATO
          </button>
        </div>
      </div>

      <div class="">
        <h2 class="font-bold text-4xl mb-5">
          Agende uma demonstração e descubra como podemos transformar seu órgão
          público
        </h2>
        <UInput
          v-model="value"
          unstyled
          :input-class="'border-b border-gray-400 focus:outline-none focus:border-blue-500 bg-transparent text-white w-full py-2'"
          placeholder="Digite algo..."
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionContact",
};
</script>
