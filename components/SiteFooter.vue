<template>
  <div class="bg-secondary text-white w-full">
    <div class="container text-gray-text">
      <div class="flex flex-col gap-8 px-3.5">
        <NuxtLink to="/" class="flex justify-start">
          <NuxtImg
            src="/assets/logo-light.png"
            alt="Logo 'GE - Gestão Expert'"
            class="w-[157px] h-[50px]"
          />
        </NuxtLink>
        <p class="font-thin text-sm/[30px] mr-8">
          A Gestão Expert oferece excelência em soluções para a gestão pública.
          Transforme a administração do seu órgão com tecnologia de ponta,
          processos otimizados e resultados comprovados. Entre em contato e
          descubra como podemos ajudar seu órgão a evoluir.
        </p>
        <form
          action=""
          class="relative border-[1px] bg-[#FFFFFF08] border-dashed border-[#ffffff66] rounded-full"
        >
          <input
            type="text"
            placeholder="Seu E-mail"
            class="w-full rounded-sm pl-5 pr-4 py-2"
          />
          <button
            class="w-full bg-primary rounded-full text-white font-bold whitespace-nowrap z-10 absolute top-1.5 right-1.5 px-5"
          >
            Quero Contratar
          </button>
        </form>
      </div>
      <div class="sub-container"></div>
      <div class="sub-container"></div>
      <div class="sub-container"></div>
    </div>
    <div class="footer-bottom border-t-2 bg-blue-200 w-full"></div>
  </div>
</template>
