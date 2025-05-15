<template>
  <div class="security-page">
    <!-- Header avec navigation -->
    <header class="security-header">
      <NuxtLink to="/blog" class="back-link">
        <Icon name="mdi:arrow-left" />
        Retour au blog
      </NuxtLink>
      <h1 class="text-4xl font-bold">Sécurité Web Complète</h1>
      <p class="text-gray-600 mt-2">Guide des bonnes pratiques et vulnérabilités OWASP</p>
    </header>

    <!-- Contenu principal -->
    <div class="security-content">
      <!-- Section Introduction -->
      <section class="intro-section">
        <h2 class="text-3xl font-bold mb-4">Pourquoi la sécurité est cruciale</h2>
        <SecurityChart />
        <CaseStudy 
          title="Exemple de faille récente"
          impact="Millions d'utilisateurs affectés"
          lesson="Importance des mises à jour"
        />
      </section>

      <!-- Section OWASP -->
      <section class="owasp-section">
        <h2 class="text-3xl font-bold mb-6">OWASP Top 10</h2>
        <div class="grid gap-6">
          <OwaspCard 
            v-for="item in owaspItems"
            :key="item.id"
            :item="item"
          />
        </div>
      </section>

      <!-- Laboratoire -->
      <SecurityLabSimple />
    </div>
  </div>
</template>

<script setup>
import SecurityLabSimple from '@/components/security/SecurityLabSimple.vue'

const owaspItems = [
  {
    id: 1,
    title: 'Injection',
    description: 'Les attaques par injection se produisent...',
    riskLevel: 'Élevé',
    solutions: [
      'Utiliser des requêtes paramétrées',
      'Valider les entrées',
      'Utiliser des ORM'
    ]
  }
]

useHead({
  title: 'Sécurité Web - Bonnes Pratiques',
  meta: [
    { name: 'description', content: 'Guide complet de sécurité web avec OWASP Top 10' }
  ]
})
</script>

<style scoped>
.security-page {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.security-header {
  margin-bottom: 3rem;
}

.back-link {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: #3b82f6;
  margin-bottom: 1rem;
}

.security-content {
  display: grid;
  gap: 4rem;
}

section {
  padding: 2rem;
  background: white;
  border-radius: 0.5rem;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
}
</style>
