<template>
  <main class="container mx-auto px-4 py-8">
    <div class="mb-8">
      <NuxtLink 
        to="/blog" 
        class="inline-flex items-center text-blue-500 hover:underline"
      >
        <Icon name="mdi:arrow-left" class="mr-1" />
        Retour au blog
      </NuxtLink>
    </div>

    <h1 class="text-4xl font-bold mb-8">Rust</h1>
    
    <article class="prose max-w-3xl">
      <h2>Le langage de programmation Rust</h2>
      <p>Pourquoi Rust est idéal pour la programmation système...</p>
      
      <h3>Sécurité mémoire</h3>
      <p>Le système de ownership et borrowing...</p>
      
      <h3>Performance</h3>
      <p>Comparaison avec C/C++...</p>
      
      <h3>WebAssembly</h3>
      <p>Développer des applications web ultra-performantes...</p>
      
      <h3>Écosystème</h3>
      <p>Les crates indispensables...</p>
    </article>
  </main>
</template>

<script setup>
useHead({
  title: 'Rust - Blog Technique',
  meta: [
    { name: 'description', content: 'Articles sur la programmation en Rust' }
  ]
})
</script>
