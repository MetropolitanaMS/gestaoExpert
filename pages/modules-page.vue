<template>
  <section>
    <div class="w-full h-full bg-white">
      <div
        class="bg-secondary bg-[url('/assets/shape/3.png')] bg-contain bg-no-repeat bg-bottom px-8 py-4 [@media(max-width:400px)]:px-0 [@media(max-width:400px)]:py-0"
      >
        <div class="px-4 [@media(max-width:400px)]:px-0 w-full">
          <div
            class="flex flex-col md:flex-row justify-between px-4 py-8 [@media(max-width:400px)]:px-0"
          >
            <h1
              class="flex items-center justify-center text-zinc-100 text-4xl font-bold"
            >
              Mapa Estratégico
            </h1>
            <div class="flex flex-col sm:flex-row mt-5 md:mt-0">
              <button
                class="bg-zinc-200 hover:bg-zinc-300 font-bold rounded-lg p-3 sm:p-4 mx-4"
              >
                Ativar licença
              </button>
              <button
                class="bg-zinc-200 hover:bg-zinc-300 font-bold rounded-lg p-3 sm:p-4 mt-3 sm:mt-0 mx-4"
              >
                Solicitar demonstração
              </button>
            </div>
          </div>
          <div class="px-4 pt-4 pb-15 mx-[15px] [@media(max-width:400px)]:px-0">
            <div class="px-[15px]">
              <p class="flex items-center justify-center text-zinc-100">
                O Gestão Fiscal é a solução para os auditores fiscais. <br />
                Possibilitando mais agilidade e controle na identificação de
                <br />
                possíveis irregularidades e uma fiscalização inteligente, que
                <br />
                auxilia no aumento da arrecadação.
              </p>
            </div>
          </div>
        </div>
        <div>
          <NuxtImg
            class="w-full h-full max-h-[500px] object-contain"
            src="/assets/dashboard/1.png"
          />
        </div>
      </div>
      <!-- Fim primeiro componente -->
      <div class="mt-5">
        <ul class="flex flex-wrap gap-5 items-center justify-center">
          <li class="flex items-center gap-2">
            <span class="text-lg">•</span>
            <a href="#" class="text-lg !text-zinc-700 hover:text-primary"
              >Benefícios</a
            >
          </li>
          <li class="flex items-center gap-2">
            <span class="text-lg">•</span>
            <a href="#" class="text-lg !text-zinc-700 hover:text-primary"
              >Mais Informações</a
            >
          </li>
          <li class="flex items-center gap-2">
            <span class="text-lg">•</span>
            <a href="#" class="text-lg !text-zinc-700 hover:text-primary"
              >Perguntas Frequentes</a
            >
          </li>
          <li class="flex items-center gap-2">
            <span class="text-lg">•</span>
            <a href="#" class="text-lg !text-zinc-700 hover:text-primary"
              >Veja o Vídeo</a
            >
          </li>
          <li class="flex items-center gap-2">
            <span class="text-lg">•</span>
            <a href="#" class="text-lg !text-zinc-700 hover:text-primary"
              >Cases</a
            >
          </li>
        </ul>
      </div>
      <!-- Fim segundo componente -->
      <div class="flex flex-col lg:flex-row items-center justify-center pt-12">
        <div class="flex flex-col lg:min-h-[320px] items-center p-5">
          <span class="text-primary">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 448 512"
              fill="currentColor"
              class="w-11 h-11 inline-block"
            >
              <path
                d="M224 256A128 128 0 1 0 224 0a128 128 0 1 0 0 256zm-45.7 48C79.8 304 0 383.8 0 482.3C0 498.7 13.3 512 29.7 512l388.6 0c16.4 0 29.7-13.3 29.7-29.7C448 383.8 368.2 304 269.7 304l-91.4 0z"
              />
            </svg>
          </span>
          <h3 class="font-bold text-xl mt-5 mb-[10px]">Social</h3>
          <p class="text-sm text-center max-w-xs">
            Com os cruzamentos da malha fiscal é possível identificar com
            celeridade sinais de evasão fiscal.
          </p>
        </div>

        <div class="flex flex-col lg:min-h-[320px] items-center p-5">
          <span class="text-primary">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 320 512"
              fill="currentColor"
              class="w-11 h-11"
            >
              <path
                d="M160 0c17.7 0 32 14.3 32 32v35.7c1.6 .2 3.1 .4 4.7 .7c.4 .1 .7 .1 1.1 .2l48 8.8c17.4 3.2 28.9 19.9 25.7 37.2s-19.9 28.9-37.2 25.7l-47.5-8.7c-31.3-4.6-58.9-1.5-78.3 6.2s-27.2 18.3-29 28.1c-2 10.7-.5 16.7 1.2 20.4c1.8 3.9 5.5 8.3 12.8 13.2c16.3 10.7 41.3 17.7 73.7 26.3l2.9 .8c28.6 7.6 63.6 16.8 89.6 33.8c14.2 9.3 27.6 21.9 35.9 39.5c8.5 17.9 10.3 37.9 6.4 59.2c-6.9 38-33.1 63.4-65.6 76.7c-13.7 5.6-28.6 9.2-44.4 11v33.4c0 17.7-14.3 32-32 32s-32-14.3-32-32v-34.9c-.4-.1-.9-.1-1.3-.2h0c-24.4-3.8-64.5-14.3-91.5-26.3c-16.1-7.2-23.4-26.1-16.2-42.2s26.1-23.4 42.2-16.2c20.9 9.3 55.3 18.5 75.2 21.6c31.9 4.7 58.2 2 76-5.3c16.9-6.9 24.6-16.9 26.8-28.9c1.9-10.6 .4-16.7-1.3-20.4c-1.9-4-5.6-8.4-13-13.3c-16.4-10.7-41.5-17.7-74-26.3l-2.8-.7c-30.4-8-65.4-17.3-91.4-34.3c-14.2-9.3-27.5-22-35.8-39.6c-8.4-17.9-10.1-37.9-6.1-59.2C23.7 116 52.3 91.2 84.8 78.3c13.3-5.3 27.9-8.9 43.2-11V32c0-17.7 14.3-32 32-32z"
              />
            </svg>
          </span>
          <h3 class="font-bold text-xl mt-5 mb-[10px]">Econômico</h3>
          <p class="text-sm text-center max-w-xs">
            Agilize a apuração fiscal ao inserir todos os dados já declarados
            pelo contribuinte no sistema de escrituração de notas fiscais
            eletrônicas municipal com apenas 1 clique.
          </p>
        </div>

        <div class="flex flex-col lg:min-h-[320px] items-center p-5">
          <span class="text-primary">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 640 512"
              fill="currentColor"
              class="w-11 h-11"
            >
              <path
                d="M480 48c0-26.5-21.5-48-48-48H336c-26.5 0-48 21.5-48 48v48h-64V24c0-13.3-10.7-24-24-24s-24 10.7-24 24v72H112V24c0-13.3-10.7-24-24-24S64 10.7 64 24v72H48C21.5 96 0 117.5 0 144v320c0 26.5 21.5 48 48 48h384h160c26.5 0 48-21.5 48-48V240c0-26.5-21.5-48-48-48H480V48zM576 368v32c0 8.8-7.2 16-16 16h-32c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16zM240 416h-32c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16v32c0 8.8-7.2 16-16 16zm-112-16c0 8.8-7.2 16-16 16H80c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16v32zM560 256c8.8 0 16 7.2 16 16v32c0 8.8-7.2 16-16 16h-32c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32zM256 176v32c0 8.8-7.2 16-16 16h-32c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16zM112 160c8.8 0 16 7.2 16 16v32c0 8.8-7.2 16-16 16H80c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32zM256 304c0 8.8-7.2 16-16 16h-32c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16v32zM112 320H80c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16v32c0 8.8-7.2 16-16 16zm304-48v32c0 8.8-7.2 16-16 16h-32c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16zM400 64c8.8 0 16 7.2 16 16v32c0 8.8-7.2 16-16 16h-32c-8.8 0-16-7.2-16-16V80c0-8.8 7.2-16 16-16h32zm16 112v32c0 8.8-7.2 16-16 16h-32c-8.8 0-16-7.2-16-16v-32c0-8.8 7.2-16 16-16h32c8.8 0 16 7.2 16 16z"
              />
            </svg>
          </span>
          <h3 class="font-bold text-xl mt-5 mb-[10px]">Urbano</h3>
          <p class="text-sm text-center max-w-xs">
            A rotina do Domicílio Tributário Eletrônico auxiliará o fisco na
            comunicação com o contribuinte.
          </p>
        </div>

        <div class="flex flex-col lg:min-h-[320px] items-center p-5">
          <span class="text-primary">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              fill="currentColor"
              class="w-11 h-11"
            >
              <path
                d="M243.4 2.6l-224 96c-14 6-21.8 21-18.7 35.8S16.8 160 32 160v8c0 13.3 10.7 24 24 24h400c13.3 0 24-10.7 24-24v-8c15.2 0 28.3-10.7 31.3-25.6s-4.8-29.9-18.7-35.8l-224-96c-8-3.4-17.2-3.4-25.2 0zM128 224H64v196.3c-.6.3-1.2.7-1.8 1.1l-48 32c-11.7 7.8-17 22.4-12.9 35.9S17.9 512 32 512h448c14.1 0 26.5-9.2 30.6-22.7s-1.1-28.1-12.9-35.9l-48-32c-.6-.4-1.2-.7-1.8-1.1V224h-64v192h-40V224h-64v192h-48V224h-64v192h-40V224zm128-160a32 32 0 1 1 0 64 32 32 0 1 1 0-64z"
              />
            </svg>
          </span>
          <h3 class="font-bold text-xl mt-5 mb-[10px]">Institucional</h3>
          <p class="text-sm text-center max-w-xs">
            Identificar o andamento do recurso de um dado contribuinte tornou-se
            uma tarefa mais simples com a rotina do Contencioso Tributário.
          </p>
        </div>
      </div>
      <!-- Fim terceiro componente -->
      <div class="flex justify-center my-5">
        <div
          class="h-1 w-full max-w-[250px] sm:max-w-[350px] md:max-w-[450px] lg:max-w-[600px] bg-primary rounded-full"
        ></div>
      </div>
      <!-- Fim quarto componente -->
      <div class="w-full max-w-5xl mx-auto px-4 my-10">
        <div class="aspect-video">
          <iframe
            class="w-full h-full"
            src="https://www.youtube.com/embed/7D2EFCYaKZo"
            title="Os mecanismos invisíveis por trás das suas decisões | Rocketseat Class"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </div>
      </div>
      <!-- Fim quinto componente -->
      <div class="flex flex-col items-center justify-center lg:mx-40 px-4">
        <h1 class="font-bold text-4xl">Benefícios</h1>
        <div
          class="h-1 my-5 w-full max-w-[250px] sm:max-w-[350px] md:max-w-[450px] lg:max-w-[600px] bg-primary rounded-full"
        ></div>
        <div class="lg:px-50 py-7">
          <div class="flex flex-col mb-5">
            <span
              class="bg-primary w-10 h-10 flex items-center justify-center rounded-full text-white"
            >
              1
            </span>
            <div class="flex flex-col justify-center items-start">
              <h4 class="font-bold text-xl py-2">Inteligência fiscal</h4>
              <p class="text-zinc-400">
                Utilize os recursos de malha fiscal da receita bruta do Simples
                Nacional, cartão de crédito, entre outras para incrementar a
                receita municipal.
              </p>
            </div>
          </div>

          <div class="flex flex-col mb-5">
            <span
              class="bg-primary w-10 h-10 flex items-center justify-center rounded-full text-white"
            >
              2
            </span>
            <div class="flex flex-col justify-center items-start">
              <h4 class="font-bold text-xl py-2">
                Agilidade na comunicação com o contribuinte
              </h4>
              <p class="text-zinc-400">
                O recurso do Domicílio Tributário permite aos auditores fiscais
                se comunicarem diretamente com o contribuinte, dando agilidade
                na resolução de dúvidas e/ou entraves.
              </p>
            </div>
          </div>

          <div class="flex flex-col mb-5">
            <span
              class="bg-primary w-10 h-10 flex items-center justify-center rounded-full text-white"
            >
              3
            </span>
            <div class="flex flex-col justify-center items-start">
              <h4 class="font-bold text-xl py-2">
                Digitalização do contencioso
              </h4>
              <p class="text-zinc-400">
                Encontrar um processo de recurso de um contribuinte agora se
                tornou muito mais fácil com a ferramenta de Controle do
                Contencioso. Trâmites, documentos e pareceres agora estão à
                distância de poucos cliques.
              </p>
            </div>
          </div>

          <div class="flex flex-col mb-5">
            <span
              class="bg-primary w-10 h-10 flex items-center justify-center rounded-full text-white"
            >
              4
            </span>
            <div class="flex flex-col justify-center items-start">
              <h4 class="font-bold text-xl py-2">
                Gestão da ciência do contribuinte
              </h4>
              <p class="text-zinc-400">
                Com a funcionalidade do registro de envio e entrega das
                notificações e intimações ficou muito mais fácil de acompanhar o
                histórico das movimentações da ciência do contribuinte.
              </p>
            </div>
          </div>

          <div class="flex flex-col mb-5">
            <span
              class="bg-primary w-10 h-10 flex items-center justify-center rounded-full text-white"
            >
              5
            </span>
            <div class="flex flex-col justify-center items-start">
              <h4 class="font-bold text-xl py-2">Gerenciamento setorizado</h4>
              <p class="text-zinc-400">
                Configure o sistema conforme as equipes de fiscalização
                existentes no município, com isso, você terá um controle maior
                dos registros pertinentes ao seu departamento.
              </p>
            </div>
          </div>
        </div>
      </div>
      <!-- Fim sexto componente -->
      <div class="lg:py-7">
        <div
          class="flex flex-col lg:flex-row lg:mx-10 min-[1600px]:mx-80 pt-0 p-12"
        >
          <div class="lg:basis-[60%]">
            <h2 class="text-3xl text-left font-semibold mt-5 mb-6">
              Setores de fiscalização
            </h2>
            <p class="text-base text-zinc-400 text-left mb-4">
              O Gestão Fiscal permite que o sistema seja configurado conforme os
              setores de fiscalização municipal. Cada setor geralmente possui um
              gestor, uma equipe e uma área de atuação. Com o setor devidamente
              configurado, basta colocar as mãos à obra. Os registros gerados
              dentro de um setor serão visualizados apenas pelas pessoas
              vinculadas ao setor.
            </p>
          </div>
          <div class="lg:basis-[40%] flex items-center justify-center">
            <NuxtImg src="/assets/dashboard/1.png" class="rounded-xl" />
          </div>
        </div>

        <div class="flex flex-col lg:flex-row lg:mx-10 min-[1600px]:mx-80 p-12">
          <div
            class="lg:basis-[40%] flex items-center justify-center order-1 lg:order-none"
          >
            <NuxtImg src="/assets/dashboard/1.png" class="rounded-xl" />
          </div>
          <div class="lg:basis-[60%]">
            <h2 class="text-3xl text-right font-semibold mt-5 mb-6">
              Inteligência fiscal
            </h2>
            <p class="text-base text-zinc-400 text-right mb-4">
              Faça uso da Inteligência Fiscal e encontre as principais
              divergências entre os contribuintes do Simples Nacional por meio
              do cruzamento da receita bruta do PGDAS-D. Confira também os
              cruzamentos dos cartórios e dos valores recebidos pelos
              contribuintes em cartão de crédito/débito.
            </p>
          </div>
        </div>

        <div class="flex flex-col lg:flex-row lg:mx-10 min-[1600px]:mx-80 p-12">
          <div class="lg:basis-[60%]">
            <h2 class="text-3xl text-left font-semibold mt-5 mb-6">
              Domicílio tributário
            </h2>
            <p class="text-base text-zinc-400 text-left mb-4">
              Permite ao fisco a comunicação direta com o contribuinte via
              sistema municipal. Adeque seu código tributário municipal para
              contemplar esta modalidade de comunicação e tenha em seu controle
              todo o histórico das conversas e faça requisições ao contribuinte
              por meio desta funcionalidade.
            </p>
          </div>
          <div class="lg:basis-[40%] flex items-center justify-center">
            <NuxtImg src="/assets/dashboard/1.png" class="rounded-xl" />
          </div>
        </div>

        <div class="flex flex-col lg:flex-row lg:mx-10 min-[1600px]:mx-80 p-12">
          <div
            class="lg:basis-[40%] flex items-center justify-center order-1 lg:order-none"
          >
            <NuxtImg src="/assets/dashboard/1.png" class="rounded-xl" />
          </div>
          <div class="lg:basis-[60%]">
            <h2 class="text-3xl text-right font-semibold mt-5 mb-6">
              Processo fiscal
            </h2>
            <p class="text-base text-zinc-400 text-right mb-4">
              O sistema conta com a gestão das ações fiscais, processo este
              responsável por registrar as intimações fiscais expedidas aos
              contribuintes, os autos de infração e a apuração fiscal. Execute
              as apurações fiscais por aqui e com base na diferença encontrada
              para o lançamento da diferença do ISS apurado.
            </p>
          </div>
        </div>

        <div class="flex flex-col lg:flex-row lg:mx-10 min-[1600px]:mx-80 p-12">
          <div class="lg:basis-[60%]">
            <h2 class="text-3xl text-left font-semibold mt-5 mb-6">
              Contencioso tributário
            </h2>
            <p class="text-base text-zinc-400 text-left mb-4">
              Agora você tem na palma da mão o controle do contencioso
              tributário. Aqui você encontrará os marcos de datas importantes
              deste processo tão complexo, fará a tramitação entre as partes
              interessadas e registrará o parecer do julgamento em 1ª e 2ª
              instância quando necessário.
            </p>
          </div>
          <div class="lg:basis-[40%] flex items-center justify-center">
            <NuxtImg src="/assets/dashboard/1.png" class="rounded-xl" />
          </div>
        </div>
      </div>
      <!-- Fim sétimo componente -->
      <div>
        <div class="flex items-center justify-center w-full">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 512 512"
            fill="currentColor"
            class="w-30 h-30 text-secondary"
          >
            <path
              d="M168.2 384.9c-15-5.4-31.7-3.1-44.6 6.4c-8.2 6-22.3 14.8-39.4 22.7c5.6-14.7 9.9-31.3 11.3-49.4c1-12.9-3.3-25.7-11.8-35.5C60.4 302.8 48 272 48 240c0-79.5 83.3-160 208-160s208 80.5 208 160s-83.3 160-208 160c-31.6 0-61.3-5.5-87.8-15.1zM26.3 423.8c-1.6 2.7-3.3 5.4-5.1 8.1l-.3 .5c-1.6 2.3-3.2 4.6-4.8 6.9c-3.5 4.7-7.3 9.3-11.3 13.5c-4.6 4.6-5.9 11.4-3.4 17.4c2.5 6 8.3 9.9 14.8 9.9c5.1 0 10.2-.3 15.3-.8l.7-.1c4.4-.5 8.8-1.1 13.2-1.9c.8-.1 1.6-.3 2.4-.5c17.8-3.5 34.9-9.5 50.1-16.1c22.9-10 42.4-21.9 54.3-30.6c31.8 11.5 67 17.9 104.1 17.9c141.4 0 256-93.1 256-208S397.4 32 256 32S0 125.1 0 240c0 45.1 17.7 86.8 47.7 120.9c-1.9 24.5-11.4 46.3-21.4 62.9zM144 272a32 32 0 1 0 0-64 32 32 0 1 0 0 64zm144-32a32 32 0 1 0 -64 0 32 32 0 1 0 64 0zm80 32a32 32 0 1 0 0-64 32 32 0 1 0 0 64z"
            />
          </svg>
        </div>

        <div class="flex items-center justify-center mt-10 mx-8 px-4">
          <h1 class="text-4xl font-bold">Perguntas frequentes</h1>
        </div>
      </div>
      <!-- Fim oitavo componente -->
      <!-- FIM  -->
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
