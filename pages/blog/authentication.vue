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

    <h1 class="text-4xl font-bold mb-8">Authentication</h1>
    
    <article class="prose max-w-3xl">
      <h2>Méthodes modernes d'authentification</h2>
      <p>Comparaison des différentes approches de sécurité...</p>
      
      <h3>JSON Web Tokens (JWT)</h3>
      <p>Implémentation sécurisée et bonnes pratiques...</p>
      
      <h3>OAuth 2.0 & OpenID Connect</h3>
      <p>Intégration avec les providers externes...</p>
      
      <h3>Authentification Multi-Facteur</h3>
      <p>Renforcement de la sécurité des comptes...</p>
    </article>
  </main>
</template>

<script setup>
useHead({
  title: 'Authentication - Blog Technique',
  meta: [
    { name: 'description', content: 'Articles sur les systèmes d\'authentification modernes' }
  ]
})
</script>
