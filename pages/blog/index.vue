<template>
  <main class="container mx-auto px-4 py-8">
    <h1 class="text-4xl font-bold mb-8">Blog Technique</h1>
    
    <div class="grid md:grid-cols-2 gap-8">
      <article 
        v-for="category in categories" 
        :key="category.id"
        class="border rounded-lg p-6 hover:shadow-md transition-shadow"
      >
        <h2 class="text-2xl font-semibold mb-3">{{ category.name }}</h2>
        <p class="text-gray-600 mb-4">{{ category.description }}</p>
        <NuxtLink 
          :to="`/blog/${category.slug}`"
          class="text-blue-500 hover:underline inline-flex items-center"
        >
          Explorer
          <Icon name="mdi:arrow-right" class="ml-1" />
        </NuxtLink>
      </article>
    </div>
  </main>
</template>

<script setup>
const categories = [
  {
    id: 1,
    name: 'Security',
    slug: 'security',
    description: 'Articles sur la sécurité web et les bonnes pratiques OWASP'
  },
  {
    id: 2,
    name: 'DevOps',
    slug: 'devops', 
    description: 'CI/CD, Docker, Kubernetes et infrastructure cloud'
  },
  {
    id: 3,
    name: 'Authentication',
    slug: 'authentication',
    description: 'JWT, OAuth 2.0 et gestion des sessions'
  },
  {
    id: 4,
    name: 'Rust',
    slug: 'rust',
    description: 'Programmation système et WebAssembly avec Rust'
  }
]
</script>
