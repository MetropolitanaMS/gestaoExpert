<script setup>
import { ref } from "vue";

const questionsList = [
  {
    question: "Como a Gestão Expert pode beneficiar meu órgão público?",
    answer:
      "A Gestão Expert oferece um conjunto completo de soluções para modernizar a gestão pública, desde o planejamento estratégico até o monitoramento de resultados. Nossos sistemas, dashboards e ferramentas de IA auxiliam na otimização de recursos, aumento da transparência e na tomada de decisões mais assertivas, impactando positivamente a eficiência do seu órgão e a qualidade dos serviços prestados à população.",
  },
  {
    question:
      "Quais os tipos de órgãos públicos que podem utilizar a Gestão Expert?",
    answer:
      "A Gestão Expert é adaptável a diferentes tipos de órgãos públicos, desde prefeituras e governos estaduais até órgãos federais e instituições do Sistema S. Nossas soluções são flexíveis e podem ser personalizadas para atender às necessidades específicas de cada órgão, independentemente do seu tamanho ou área de atuação.",
  },
  {
    question: "Como posso obter mais informações sobre a Gestão Expert?",
    answer:
      "Entre em contato conosco através do formulário nesta página, por telefone ou e-mail. Nossa equipe terá prazer em apresentar a Gestão Expert em detalhes, entender as suas necessidades e oferecer a melhor solução para o seu órgão público. Também convidamos você a explorar nosso site e conhecer nossos cases de sucesso.",
  },
];

const activeIndex = ref(null);

function toggleAccordion(index) {
  activeIndex.value = activeIndex.value === index ? null : index;
}
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
        <ul class="flex flex-col gap-8">
          <li
            class="card cursor-pointer"
            v-for="(question, index) in questionsList"
            :key="index"
          >
            <div
              class="flex justify-between items-start"
              @click="toggleAccordion(index)"
            >
              <h4 class="text-lg font-semibold">
                {{ question.question }}
              </h4>
              <Icon
                name="material-symbols:keyboard-arrow-down-rounded"
                size="24"
                :class="{
                  '-rotate-90': activeIndex !== index,
                  'rotate-0': activeIndex === index,
                }"
                :style="{ color: activeIndex === index ? 'black' : '' }"
                class="hover:cursor-pointer text-gray-text transition-transform py-3 px-3 sm:px-4 md:px-5 lg:px-6 xl:px-7 2xl:px-8"
              />
            </div>
            <transition
              name="accordion"
              @enter="(el) => (el.style.height = el.scrollHeight + 'px')"
              @leave="(el) => (el.style.height = '0px')"
            >
              <div
                v-if="activeIndex === index"
                class="accordion-content overflow-hidden"
              >
                <div
                  class="pt-3.5 mt-5 border-t-[1px] border-[#e7e7e7] text-black-paragraph"
                >
                  <p>{{ question.answer }}</p>
                </div>
              </div>
            </transition>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.accordion-enter-active,
.accordion-leave-active {
  transition: height 0.3s ease, opacity 0.3s ease;
  overflow: hidden;
}

.accordion-enter-from,
.accordion-leave-to {
  height: 0 !important;
  opacity: 0;
}

.accordion-content {
  transition: height 0.3s ease;
  height: auto;
}
</style>
