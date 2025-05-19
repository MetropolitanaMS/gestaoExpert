<template>
  <header
    class="flex flex-row bg-white text-black shadow-md text-sm items-center h-fit w-full sticky top-0 z-50"
  >
    <div class="flex flex-row px-8 py-4 lg:mx-10 w-full justify-between">
      <NuxtLink class="flex justify-center items-center" to="/">
        <button
          type="button"
          class="flex flex-row justify-center items-center cursor-pointer"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="w-6 h-6 text-black rotate-180"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M9 5l7 7-7 7"
            />
          </svg>
          <span class="font-bold">Voltar</span>
        </button>
      </NuxtLink>
      <NuxtImg
        src="/assets/logo.png"
        alt="Logo 'GE - Gestão Expert'"
        class="w-[90px] lg:w-[115px] h-[40px] lg:h-[50px]"
      />
    </div>
  </header>
</template>
