<script setup>
const questionsList = [
  {
    question: "Como a Gestão Expert pode beneficiar meu órgão público?",
    answer:
      "O processo de compra é simples e rápido. Você pode entrar em contato conosco através do nosso site ou telefone, e nossa equipe irá guiá-lo em cada etapa.",
  },
  {
    question:
      "Quais os tipos de órgãos públicos que podem utilizar a Gestão Expert?",
    answer:
      "O processo de compra é simples e rápido. Você pode entrar em contato conosco através do nosso site ou telefone, e nossa equipe irá guiá-lo em cada etapa.",
  },
  {
    question: "Como posso obter mais informações sobre a Gestão Expert?",
    answer:
      "O processo de compra é simples e rápido. Você pode entrar em contato conosco através do nosso site ou telefone, e nossa equipe irá guiá-lo em cada etapa.",
  },
];
</script>

<template>
  <section class="w-full flex justify-center items-center pt-10 pb-12" id="faq">
    <div
      class="w-full max-w-[540px] sm:max-w-[720px] md:max-w-[960px] flex flex-col justify-center items-center lg:grid lg:grid-cols-2 gap-8 px-3.5 lg:px-0"
    >
      <div class="w-full flex justify-center items-center px-3.5">
        <NuxtImg
          src="/assets/illustration/9.png"
          alt="Illustração de uma pessoa segurando um ponto de interrogação e um balão de fala com reticências sobre a sua cabeça."
          class="w-full"
        />
      </div>
      <div class="flex flex-col gap-8 text-start px-3.5">
        <h2 class="font-bold text-3xl lg:text-4xl text-black-text capitalize">
          perguntas frequentes
        </h2>
        <ul class="accordion flex flex-col gap-8">
          <li
            class="card cursor-pointer"
            v-for="(question, index) in questionsList"
            :key="index"
          >
            <div class="card-header flex justify-between items-start">
              <h4 class="text-lg font-semibold">
                {{ question.question }}
              </h4>
              <Icon
                name="material-symbols:keyboard-arrow-down-rounded"
                size="24"
                class="hover:cursor-pointer text-gray-text rotate-[270deg] py-3 px-3 sm:px-4 md:px-5 lg:px-6 xl:px-7 2xl:px-8"
              />
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
