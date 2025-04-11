<script setup lang="ts">
const isPanelVisible = ref(false);

const navItems = [
  { href: "https://aderencia.com.br", text: "ADERÊNCIA" },
  { href: "#benefits", text: "BENEFÍCIOS" },
  { href: "#features", text: "FUNCIONALIDADES" },
  { href: "#faq", text: "FAQ" },
  { href: "#contact", text: "CONTATO" },
];
</script>

<template>
  <header
    class="bg-white text-black shadow-md text-sm flex flex-col justify-center items-center h-fit w-full sticky top-0 z-50"
    id="site-header"
  >
    <div
      class="w-full bg-white flex justify-center items-center px-8 py-4 lg:px-9 lg:border-b lg:border-white z-40"
    >
      <div
        class="w-full max-w-[1140px] grid grid-cols-3 items-center lg:flex lg:justify-between lg:gap-8"
      >
        <div class="lg:hidden">
          <Icon
            name="mdi:menu"
            size="24"
            class="hover:cursor-pointer text-primary"
            @click="isPanelVisible = true"
          />
        </div>
        <div class="w-full flex justify-center lg:justify-start">
          <NuxtLink to="#hero">
            <NuxtImg
              src="/assets/logo.png"
              alt="Logo 'GE - Gestão Expert'"
              class="w-[90px] lg:w-[115px] h-[40px] lg:h-[50px]"
            />
          </NuxtLink>
        </div>
        <div class="hidden lg:block">
          <ul class="flex gap-8 justify-center items-center lg:w-full">
            <li
              v-for="(item, index) in navItems"
              :key="index"
              class="text-black-text"
            >
              <div
                class="hover:text-primary w-fit transition duration-200 ease-in-out"
              >
                <NuxtLink :to="item.href" class="font-bold py-2">{{
                  item.text
                }}</NuxtLink>
              </div>
            </li>
          </ul>
        </div>
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
