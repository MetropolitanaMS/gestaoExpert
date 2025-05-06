<template>
  <div id="contact" class="py-28 relative">
    <div class="flex flex-wrap lg:flex-nowrap mx-4 xl:mx-28 px-3.5">
      <div class="flex flex-col items-center px-3.5">
        <div
          class="flex flex-col w-full items-center rounded-md bg-secondary p-9 mr-5"
        >
          <div
            class="rounded-full shadow-inner bg-[#353266] border-1 border-dashed border-[#ffffff80] p-6 inline-flex items-center justify-center mb-6"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              fill="currentColor"
              class="w-8 h-8 text-white"
            >
              <path
                d="M280 0C408.1 0 512 103.9 512 232c0 13.3-10.7 24-24 24s-24-10.7-24-24c0-101.6-82.4-184-184-184c-13.3 0-24-10.7-24-24s10.7-24 24-24zm8 192a32 32 0 1 1 0 64 32 32 0 1 1 0-64zm-32-72c0-13.3 10.7-24 24-24c75.1 0 136 60.9 136 136c0 13.3-10.7 24-24 24s-24-10.7-24-24c0-48.6-39.4-88-88-88c-13.3 0-24-10.7-24-24zM117.5 1.4c19.4-5.3 39.7 4.6 47.4 23.2l40 96c6.8 16.3 2.1 35.2-11.6 46.3L144 207.3c33.3 70.4 90.3 127.4 160.7 160.7L345 318.7c11.2-13.7 30-18.4 46.3-11.6l96 40c18.6 7.7 28.5 28 23.2 47.4l-24 88C481.8 499.9 466 512 448 512C200.6 512 0 311.4 0 64C0 46 12.1 30.2 29.5 25.4l88-24z"
              />
            </svg>
          </div>
          <p class="text-center text-white text-sm mb-4 leading-8">
            Quer ser nosso parceiro? Entre em contato agora mesmo! Oferecemos
            suporte completo e oportunidades de crescimento conjunto.
          </p>
          <button
            type="button"
            class="w-full px-3.5 h-12 cursor-pointer rounded-sm text-secondary font-bold bg-white hover:bg-primary hover:text-white transition-colors duration-300 ease-in-out mt-7"
          >
            ENTRAR EM CONTATO
          </button>
        </div>
      </div>

      <div class="px-5">
        <h2 class="font-bold text-4xl mb-5 mt-5 lg:mt-0">
          Agende uma demonstração e descubra como podemos transformar seu órgão
          público
        </h2>
        <form action="submit">
          <div
            class="group flex w-full items-center border-b border-gray-300 mb-4"
          >
            <svg
              class="w-5 h-5 mr-4 text-gray-400 transition-colors duration-300 group-focus-within:text-secondary"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 448 512"
              fill="currentColor"
            >
              <path
                d="M224 256A128 128 0 1 0 224 0a128 128 0 1 0 0 256zm-45.7 48C79.8 304 0 383.8 0 482.3C0 498.7 13.3 512 29.7 512l388.6 0c16.4 0 29.7-13.3 29.7-29.7C448 383.8 368.2 304 269.7 304l-91.4 0z"
              />
            </svg>

            <input
              type="text"
              placeholder="Nome"
              class="w-full bg-transparent py-2 outline-none placeholder-gray-400"
            />
          </div>
          <div class="flex flex-col lg:flex-row relative w-full mb-4">
            <div
              class="group flex w-full items-center border-b border-gray-300 mb-5 lg:mb-0 lg:mr-3.5"
            >
              <svg
                class="w-5 h-5 text-gray-400 mr-4 transition-colors duration-300 group-focus-within:text-secondary"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
                fill="currentColor"
              >
                <path
                  d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48L48 64zM0 176L0 384c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-208L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"
                />
              </svg>

              <input
                type="tel"
                placeholder="Email*"
                class="w-full bg-transparent py-2 outline-none placeholder-gray-400"
              />
            </div>
            <div
              class="group flex w-full items-center border-b border-gray-300 lg:ml-3.5"
            >
              <svg
                class="w-5 h-5 text-gray-400 mr-4 transition-colors duration-300 group-focus-within:text-secondary"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
                fill="currentColor"
              >
                <path
                  d="M347.1 24.6c7.7-18.6 28-28.5 47.4-23.2l88 24C499.9 30.2 512 46 512 64c0 247.4-200.6 448-448 448c-18 0-33.8-12.1-38.6-29.5l-24-88c-5.3-19.4 4.6-39.7 23.2-47.4l96-40c16.3-6.8 35.2-2.1 46.3 11.6L207.3 368c70.4-33.3 127.4-90.3 160.7-160.7L318.7 167c-13.7-11.2-18.4-30-11.6-46.3l40-96z"
                />
              </svg>
              <input
                type="tel"
                placeholder="Telefone"
                class="w-full bg-transparent py-2 outline-none placeholder-gray-400"
              />
            </div>
          </div>
          <div
            class="group flex w-full items-center border-b border-gray-300 mb-4"
          >
            <svg
              class="w-5 h-5 text-gray-400 mr-4 transition-colors duration-300 group-focus-within:text-secondary"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              fill="currentColor"
            >
              <path
                d="M471.6 21.7c-21.9-21.9-57.3-21.9-79.2 0L362.3 51.7l97.9 97.9 30.1-30.1c21.9-21.9 21.9-57.3 0-79.2L471.6 21.7zm-299.2 220c-6.1 6.1-10.8 13.6-13.5 21.9l-29.6 88.8c-2.9 8.6-.6 18.1 5.8 24.6s15.9 8.7 24.6 5.8l88.8-29.6c8.2-2.7 15.7-7.4 21.9-13.5L437.7 172.3 339.7 74.3 172.4 241.7zM96 64C43 64 0 107 0 160L0 416c0 53 43 96 96 96l256 0c53 0 96-43 96-96l0-96c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 96c0 17.7-14.3 32-32 32L96 448c-17.7 0-32-14.3-32-32l0-256c0-17.7 14.3-32 32-32l96 0c17.7 0 32-14.3 32-32s-14.3-32-32-32L96 64z"
              />
            </svg>

            <input
              type="text"
              placeholder="Você representa qual instituição?*"
              class="w-full bg-transparent py-2 outline-none placeholder-gray-400"
            />
          </div>
          <div class="flex mt-5">
            <button
              class="flex cursor-pointer hover:bg-secondary hover:text-white transition-colors duration-300 ease-in-out items-center gap-2 border-2 border-secondary font-bold rounded-4xl mt-5 px-9 py-2.5"
              type="button"
            >
              Enviar Mensagem

              <svg
                class="w-4 h-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
                fill="currentColor"
              >
                <path
                  d="M498.1 5.6c10.1 7 15.4 19.1 13.5 31.2l-64 416c-1.5 9.7-7.4 18.2-16 23s-18.9 5.4-28 1.6L284 427.7l-68.5 74.1c-8.9 9.7-22.9 12.9-35.2 8.1S160 493.2 160 480l0-83.6c0-4 1.5-7.8 4.2-10.8L331.8 202.8c5.8-6.3 5.6-16-.4-22s-15.7-6.4-22-.7L106 360.8 17.7 316.6C7.1 311.3 .3 300.7 0 288.9s5.9-22.8 16.1-28.7l448-256c10.7-6.1 23.9-5.5 34 1.4z"
                />
              </svg>
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionContact",
};
</script>
