<template>
  <section class="bg-white py-14" id="benefits">
    <div class="w-full flex justify-center items-center">
      <div
        class="w-full max-w-[540px] md:max-w-[720px] px-3.5 flex flex-col gap-8 items-center"
      >
        <h2 class="font-bold leading-6 text-3xl text-[#333]">Benefícios</h2>
        <div class="w-full max-w-[70px] flex justify-between gap-1">
          <div class="h-0.5 w-1/6 bg-primary rounded-full"></div>
          <div class="h-0.5 w-full bg-primary rounded-full"></div>
        </div>
        <p class="text-[#666] text-center leading-7">
          Conheça os benefícios de se ter um software integrado para uma Gestão
          Pública Inteligente e Eficiente.
        </p>
      </div>
    </div>
    <div class="w-full">
      <div class="px-3.5 pt-8">
        <CarrosselComponent />
      </div>
    </div>
  </section>
</template>
