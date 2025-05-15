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

    <h1 class="text-4xl font-bold mb-8">DevOps</h1>
    
    <article class="prose max-w-3xl">
      <h2>CI/CD avec GitHub Actions</h2>
      <p>Automatisation des déploiements avec des workflows efficaces...</p>
      
      <h3>Docker</h3>
      <p>Optimisation des images et bonnes pratiques...</p>
      
      <h3>Kubernetes</h3>
      <p>Gestion des clusters et déploiements scalables...</p>
      
      <h3>Infrastructure as Code</h3>
      <p>Terraform et Pulumi pour une infrastructure reproductible...</p>
    </article>
  </main>
</template>

<script setup>
useHead({
  title: 'DevOps - Blog Technique',
  meta: [
    { name: 'description', content: 'Articles sur les pratiques DevOps modernes' }
  ]
})
</script>
