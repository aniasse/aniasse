<template>
  <footer class="w-full background-grid--fade-top background-grid pb-12 mt-20 pt-20">
    <div class="flex w-full px-14 justify-between flex-wrap">
      <!-- left -->
      <div class="text-sm max-w-[300px]">
        <p class="font-bold text-slate-600">À propos de moi</p>
        <p class="text-slate-700 mt-3">
          Je suis huynamboz, un <strong>développeur front-end</strong> du Vietnam. J'ai une riche expérience dans la conception et la personnalisation de sites web.
        </p>
        <div class="flex mt-5 gap-5">
          <NuxtLink to="https://github.com/huynamboz" target="_blank">
            <Icon name="uil:github" size="24" color="black" />
          </NuxtLink>
          <NuxtLink to="https://www.linkedin.com/in/huynamboz" target="_blank">
            <Icon name="pajamas:linkedin" size="22" color="black" />
          </NuxtLink>
        </div>
      </div>
      <!-- right -->
      <div class="flex gap-20">
        <div class="text-sm">
          <p class="font-bold text-slate-500">Découverte</p>
          <div class="flex flex-col mt-4 gap-5">
            <NuxtLink to="/projects" class="flex items-center gap-2 text-sm font-bold text-slate-600">
              <span>Projets</span>
            </NuxtLink>
            <NuxtLink to="/blog" class="flex items-center gap-2 text-sm font-bold text-slate-600">
              <span>Blog</span>
            </NuxtLink>
            <NuxtLink to="/contact" class="flex items-center gap-2 text-sm font-bold text-slate-600">
              <span>Contact</span>
            </NuxtLink>
          </div>
        </div>
        <div class="text-sm">
          <p class="font-bold text-slate-500">Ce site</p>
          <div class="flex flex-col mt-4 gap-5">
            <NuxtLink to="/" class="flex items-center gap-2 text-sm font-bold text-slate-600">
              <span>Code source</span>
            </NuxtLink>
            <NuxtLink to="https://github.com/huynamboz/huynamboz.github.io" class="flex items-center gap-2 text-sm font-bold text-slate-600">
              <span>Mon GitHub</span>
            </NuxtLink>
            <NuxtLink to="/" class="flex items-center gap-2 text-sm font-bold text-slate-600">
              <span>Crédit design</span>
              <Icon name="material-symbols-light:open-in-new" size="16" color="black" />
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
    <div class="w-full flex justify-between px-14">
      <div class="text-xs font-bold text-slate-500 mt-10">
        <span>© 2023 huynamboz</span>
      </div>
      <NuxtLink to="https://github.com/huynamboz/huynamboz.github.io" class="flex items-center gap-2 text-xs font-light text-slate-600 mt-10">
        Voir les mises à jour récentes sur GitHub
        <img src="https://komarev.com/ghpvc/?username=huynamboz" alt="" />
      </NuxtLink>
    </div>
  </footer>
</template>

<script setup>
// Importations si nécessaires
</script>

<style scoped>
/* Styles spécifiques au footer */
.background-grid {
  background-image: linear-gradient(to right, #f1f5f9 1px, transparent 1px),
                    linear-gradient(to bottom, #f1f5f9 1px, transparent 1px);
  background-size: 24px 24px;
}
.background-grid--fade-top {
  mask-image: linear-gradient(to bottom, transparent, black 20%);
}
</style>
