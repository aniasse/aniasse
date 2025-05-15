<template>
  <div class="content-wrapper container relative pt-20 pb-10">
    <div class="flex flex-col h-full">
      <!-- title content -->
      <div>
        <p class="text-4xl text-slate-600">hi! ✌️</p>
        <span class="text-slate-700 dark:text-slate-300">
          <h1
            v-motion="{
              initial: { opacity: 0, x: -100 },
              enter: { opacity: 1, x: 0, scale: 1 },
            }"
            class="opacity-0 max-md:w-[50%] mb-4 block text-[2.5rem] font-[1000] leading-none md:mb-6 md:text-7xl"
          >
            I'm
            <strong class="relative text-accent-600 dark:text-accent-500"  style="color: #FFA500;">Adama</strong>
            Niasse,
          </h1>
          <!-- <ClientOnly>
          </ClientOnly> -->
          <h2
            v-motion="{
              initial: { opacity: 0, x: -100 },
              enter: { opacity: 1, x: 0, scale: 1 },
              delay: 100,
            }"
            class="opacity-0 block text-base text-slate-600 md:text-xl dark:text-slate-400"
          >
            <span class="lowercase">A </span>
            <strong class="font-bold lowercase text-slate-700 dark:text-slate-300"
              >Full Stack Developer</strong
            >
            | networking | cybersecurity
            <span class="block">Passionate about building secure and scalable systems.</span>
          </h2>
          <!-- <ClientOnly>
          </ClientOnly> -->
        </span>
        <div
          v-motion
          :initial="{ opacity: 0, x: -100 }"
          :enter="{ opacity: 1, x: 0, scale: 1 }"
          :delay="200"
          class="opacity-0 flex items-center mt-8 gap-5"
        >
          <a href="https://www.linkedin.com/in/adama-niasse" target="_blank">
            <button
              class="px-8 py-3 text-base font-semibold text-white transition duration-200 ease-in-out transform bg-accent-600 rounded-xl hover:bg-accent-500 hover:scale-105"
            >
              About me
            </button>
          </a>
          <button class="flex gap-1 font-bold text-sm text-slate-700 items-center">
            <span class="mr-1 text-xl">👋</span>
            CONTACT
            <a href="https://www.linkedin.com/in/adama-niasse" target="_blank">
              <Icon name="pajamas:linkedin" size="20" class="ml-1" />
            </a>
            <a href="https://github.com/adama-niasse" target="_blank">
              <Icon name="mdi:github" size="20" class="ml-1" />
            </a>
          </button>
        </div>
      </div>
      <!-- end title content -->
      <!-- list icon tech -->
      <div
        v-motion
        :initial="{ opacity: 0, x: -100 }"
        :enter="{ opacity: 1, x: 0, scale: 1 }"
        :delay="300"
        class="opacity-0 mt-32 flex flex-col text-sm gap-2 font-medium text-slate-500"
      >
        <p>My favorite tech stack & tools:</p>
        <div class="flex gap-4">
          <div title="Golang">
            <Icon class="hover:text-[#00ADD8]" name="file-icons:go" size="30" />
          </div>
          <div title="Rust">
            <Icon class="hover:text-[#DEA01B]" name="mdi:language-rust" size="24" />
          </div>
          <div title="JavaScript">
    <Icon class="hover:text-[#F7DF1E]" name="mdi:language-javascript" size="24" />
  </div>
  <div title="MySQL">
    <Icon class="hover:text-[#4479A1]" name="mdi:database" size="24" />
  </div>
          <div title="VueJS">
            <Icon class="hover:text-[#52b983]" name="ri:vuejs-fill" size="26" />
          </div>
          <div title="GraphQL">
            <Icon class="hover:text-[#E10098]" name="mdi:graphql" size="26" />
          </div>
          <!-- separate -->
          <div class="h-[25px] border-r-[1px]"></div>

          <div title="Docker">
            <Icon class="hover:text-[#2496ED]" name="mdi:docker" size="24" />
          </div>
          <div title="Git">
            <Icon class="hover:text-[#d34d35]" name="cib:git" size="24" />
          </div>
        </div>
      </div>
      <!-- end list icon tech -->
    </div>
    <NuxtImg
  format="webp"
  src="/images/adama.png"
  alt="hero"
  class="absolute top-0 right-10 w-[36%] md:w-[33%] lg:w-[36%] md:top-0 xl:w-[39%] rounded-lg shadow-neon border-2 border-neon-green transform transition-transform duration-500 hover:scale-105 hover:rotate-3 filter grayscale hover:grayscale-0"
/>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
// .shadow-neon {
//     box-shadow: 0 0 10px #00FFFF, 0 0 20px #00FFFF, 0 0 30px #00FFFF;
//   }

  .border-neon-green {
    border-color: #00FF00;
  }</style>
