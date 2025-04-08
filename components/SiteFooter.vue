<script setup>
const footerLinks = [
  {
    title: "Link Rápido",
    target: "_self",
    links: [
      {
        title: "Topo",
        link: "#home",
      },
      {
        title: "Benefícios",
        link: "#benefits",
      },
      {
        title: "Funcionalidades",
        link: "#features",
      },
      {
        title: "FAQ",
        link: "#faq",
      },
      {
        title: "Contato",
        link: "#contact",
      },
    ],
  },
  {
    title: "Aderência",
    target: "_blank",
    links: [
      {
        title: "Sobre Nós",
        link: "https://aderencia.com.br/2021/sobre/",
      },
      {
        title: "Serviços",
        link: "https://aderencia.com.br/#servicos",
      },
      {
        title: "Soluções",
        link: "https://aderencia.com.br/#solucoes",
      },
      {
        title: "Contato",
        link: "https://aderencia.com.br/#contato",
      },
    ],
  },
];
</script>

<template>
  <footer class="bg-secondary w-full py-12 relative">
    <div class="absolute bottom-0 left-0 opacity-50">
      <NuxtImg
        src="/assets/shape/footer-bg.png"
        alt="Imagem de fundo do rodapé"
        class="w-full h-full"
      />
    </div>
    <div class="w-full h-full flex justify-center items-center relative z-10">
      <div
        class="text-gray-text pb-12 grid grid-cols-1 gap-12 px-3.5 max-w-[540px] md:grid-cols-2 md:max-w-[720px] md:mt-20 lg:grid-cols-4 lg:max-w-[960px] xl:max-w-[1400px]"
      >
        <div class="flex flex-col gap-8">
          <NuxtLink to="/" class="flex justify-start">
            <NuxtImg
              src="/assets/logo-light.png"
              alt="Logo 'GE - Gestão Expert'"
              class="w-[157px] h-[50px]"
            />
          </NuxtLink>
          <p class="text-[15px]/[30px] mr-8">
            A Gestão Expert oferece excelência em soluções para a gestão
            pública. Transforme a administração do seu órgão com tecnologia de
            ponta, processos otimizados e resultados comprovados. Entre em
            contato e descubra como podemos ajudar seu órgão a evoluir.
          </p>
          <form
            action="submit"
            class="relative border-[1px] bg-[#FFFFFF08] border-dashed border-[#ffffff66] rounded-full"
          >
            <input
              type="text"
              placeholder="Seu E-mail"
              class="w-full h-14 rounded-sm pl-5 pr-4 py-2 focus:outline-primary focus:outline-2 focus:outline-offset-1"
            />
            <button
              @click="console.log('enviar formulário')"
              class="w-fit absolute top-1.5 right-1.5 px-5 py-2.5 z-10 bg-primary rounded-full text-white font-bold whitespace-nowrap hover:cursor-pointer hover:bg-[#6563ad] active:bg-primary/40 transition duration-200 ease-in-out"
            >
              Quero Contratar
            </button>
          </form>
        </div>
        <div
          class="flex flex-col gap-8"
          v-for="(section, index) in footerLinks"
          :key="index"
        >
          <h4 class="text-lg text-white font-bold capitalize">
            {{ section.title }}
          </h4>
          <ul class="flex flex-col gap-5">
            <li
              v-for="(link, teste) in section.links"
              :key="teste"
              class="w-fit hover:text-white transition duration-200 ease-in-out"
            >
              <a
                :href="link.link"
                :target="section.target"
                class="w-fit flex items-center gap-1"
              >
                <Icon name="mdi:chevron-right" size="20" />
                {{ link.title }}
              </a>
            </li>
          </ul>
        </div>
        <div class="flex flex-col gap-8">
          <h4 class="text-lg text-white font-bold capitalize">Contato</h4>
          <ul class="flex flex-col gap-5">
            <li class="w-full flex items-start gap-2">
              <Icon
                name="mdi:home"
                size="24"
                class="text-primary flex-shrink-0 mr-2"
              />
              <div class="flex flex-col gap-2 flex-grow">
                <h4 class="text-white"><strong>Endereço:</strong></h4>
                <p class="break-words">
                  Avenida Mato Grosso, 3590, Campo Grande - MS - CEP 79.021-003
                </p>
              </div>
            </li>
            <li class="w-full flex items-start gap-2">
              <Icon name="mdi:email" size="24" class="text-primary" />
              <div class="flex flex-col gap-2">
                <h4 class="text-white"><strong>E-mail:</strong></h4>
                <a h-ref="mailto:info@validtheme.com"
                  ><p
                    class="hover:text-white/85 cursor-pointer transition duration-200 ease-in-out"
                  >
                    contato@aderencia.com.br
                  </p></a
                >
              </div>
            </li>
            <li class="w-full flex items-start gap-2">
              <Icon name="mdi:phone" size="24" class="text-primary" />
              <div class="flex flex-col gap-2">
                <h4 class="text-white">Telefone:</h4>
                <a href="tel:+556732110585">
                  <p
                    class="hover:text-white/85 cursor-pointer transition duration-200 ease-in-out"
                  >
                    (67) 3211-0585
                  </p>
                </a>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="border-t-[0.5px] border-[#ffffff15] w-full">
      <p class="text-center text-[15px]/[30px] pt-8 text-[#CCC]">
        © Copyright 2025. Todos direitos reservados para
        <a href="https://aderencia.com.br" target="_blank"
          ><strong class="text-primary">Aderência</strong></a
        >
      </p>
    </div>
  </footer>
</template>
