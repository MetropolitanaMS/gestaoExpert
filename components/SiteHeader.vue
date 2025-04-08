<script setup lang="ts">
const isPanelVisible = ref(false);

const navItems = [
  { href: "/aderencia", text: "ADERÊNCIA" },
  { href: "/beneficios", text: "BENEFÍCIOS" },
  { href: "/funcionalidades", text: "FUNCIONALIDADES" },
  { href: "/faq", text: "FAQ" },
  { href: "/contato", text: "CONTATO" },
];
</script>

<template>
  <header
    class="bg-white text-black shadow-md text-sm flex flex-col justify-center items-center h-fit w-full sticky top-0 z-50"
  >
    <div
      id="site-header"
      class="w-full bg-white flex justify-center items-center px-8 py-4 lg:px-9 lg:border-b lg:border-white z-40"
    >
      <div class="w-full max-w-[1320px] grid grid-cols-3 items-center">
        <Icon
          name="mdi:menu"
          size="24"
          class="hover:cursor-pointer text-primary"
          @click="isPanelVisible = true"
        />
        <NuxtLink to="/" class="flex justify-center">
          <NuxtImg
            src="/assets/logo.png"
            alt="Logo 'GE - Gestão Expert'"
            class="w-[90px] h-[40px]"
          />
        </NuxtLink>
        <div class="w-full flex justify-end items-center">
          <button
            class="w-fit px-8 py-2.5 bg-primary text-white rounded-full hidden sm:block hover:cursor-pointer hover:bg-secondary/70 active:bg-secondary/90 transition duration-200 ease-in-out"
          >
            Demonstração
          </button>
        </div>
      </div>
    </div>
  </header>
  <SlideOverComponent
    :isVisible="isPanelVisible"
    @close="isPanelVisible = false"
  >
    <template #title>
      <NuxtLink
        to="/"
        @click="isPanelVisible = false"
        class="flex justify-center"
      >
        <NuxtImg
          src="/assets/logo.png"
          alt="Logo 'GE - Gestão Expert'"
          class="w-[90px] h-[40px]"
        />
      </NuxtLink>
    </template>
    <template #content>
      <div class="flex flex-col gap-4">
        <ul class="flex flex-col gap-4">
          <li v-for="(item, index) in navItems" :key="index" link>
            <NuxtLink
              :to="item.href"
              @click="isPanelVisible = false"
              class="font-medium text-gray-900 hover:text-lg py-2"
              >{{ item.text }}</NuxtLink
            >
          </li>
        </ul>
      </div>
    </template>
  </SlideOverComponent>
</template>
