<template>
  <section>
    <div class="w-full h-full bg-white">
      <div
        class="bg-secondary bg-[url('/assets/shape/3.png')] bg-contain bg-no-repeat bg-bottom px-8 py-4"
      >
        <div class="px-4 w-full">
          <div class="flex flex-row justify-between px-4 py-8">
            <h1 class="flex items-center text-4xl font-bold">Conteúdo</h1>
            <div>
              <button
                class="bg-zinc-200 hover:bg-zinc-300 font-bold rounded-lg p-4 mx-4"
              >
                Ativar licença
              </button>
              <button
                class="bg-zinc-200 hover:bg-zinc-300 font-bold rounded-lg p-4 mx-4"
              >
                Solicitar demonstração
              </button>
            </div>
          </div>
          <div>
            <p class="flex items-center justify-center">
              O Gestão Fiscal é a solução para os auditores fiscais.
              Possibilitando mais agilidade e controle na identificação de
              possíveis irregularidades e uma fiscalização inteligente, que
              auxilia no aumento da arrecadação.
            </p>
          </div>
        </div>
      </div>

      <!-- QUEBRA (CONTINUAR MEXENDO COM ESPAÇAMENTOS DO PARÁGRAFO) -->
    </div>
  </section>
</template>

<script setup>
definePageMeta({
  layout: "modules-layout",
});
</script>

<style>
.primary-color {
  color: #555392;
}

.secondary-color {
  color: #272455;
}
</style>
