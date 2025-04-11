<script setup>
const cteList = [
  "Modernize sua gestão",
  "Monitore resultados",
  "Otimize seus recursos",
];
</script>

<template>
  <div class="relative">
    <div
      class="w-full absolute -left-[140px] lg:-left-[240px] -top-[70px] opacity-5"
    >
      <NuxtImg
        src="/assets/shape/7.png"
        alt="Forma abstrata."
        class="w-full align-middle"
      />
    </div>
    <div class="w-full mb-40 flex justify-center items-center">
      <div
        class="flex flex-col justify-center items-center gap-7 lg:grid lg:grid-cols-2 lg:max-w-[960px] lg:gap-0"
      >
        <div class="px-3.5 max-w-[90%]">
          <NuxtImg
            src="/assets/dashboard/5.png"
            alt="Ilustração de 3 pessoas construido uma aplicação de um celular com objetos ilustrados."
            class="w-full align-middle"
          />
        </div>
        <div
          class="px-3.5 text-center flex flex-col items-center gap-8 lg:items-start lg:text-left"
        >
          <h2 class="font-bold text-black-text text-3xl leading-1.2">
            Resultados que transformam a gestão pública
          </h2>
          <p class="text-[#666666]">
            A Gestão Expert simplifica a administração do seu órgão, desde o
            planejamento estratégico até o monitoramento de resultados.
          </p>
          <ul class="flex flex-col gap-4">
            <li
              v-for="(item, index) in cteList"
              :key="index"
              class="flex gap-2"
            >
              <Icon
                name="mdi:checkbox-marked-circle"
                size="20"
                class="text-primary"
              />
              <p class="font-semibold text-black-text">{{ item }}</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
