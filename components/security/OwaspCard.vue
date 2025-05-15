<template>
  <div class="owasp-card">
    <div class="owasp-card-header">
      <span class="owasp-rank">#{{ item.id }}</span>
      <h3>{{ item.title }}</h3>
      <span class="risk-level" :class="item.riskClass">
        {{ item.riskLevel }}
      </span>
    </div>
    
    <div class="owasp-card-body">
      <p>{{ item.description }}</p>
      
      <div class="attack-example">
        <h4>Exemple d'attaque :</h4>
        <pre><code>{{ item.attackExample }}</code></pre>
      </div>
      
      <div class="solutions">
        <h4>Solutions :</h4>
        <ul>
          <li v-for="(solution, index) in item.solutions" :key="index">
            {{ solution }}
          </li>
        </ul>
      </div>
      
      <div class="resources" v-if="item.resources">
        <h4>Ressources :</h4>
        <ul>
          <li v-for="(resource, index) in item.resources" :key="index">
            <a :href="resource.url" target="_blank">{{ resource.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  item: {
    type: Object,
    required: true,
    validator: (value) => {
      return [
        'id',
        'title',
        'description',
        'riskLevel',
        'riskClass',
        'attackExample',
        'solutions'
      ].every(key => key in value)
    }
  }
})
</script>

<style scoped>
.owasp-card {
  border: 1px solid #e5e7eb;
  border-radius: 0.5rem;
  overflow: hidden;
  margin-bottom: 1.5rem;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
}

.owasp-card-header {
  background-color: #f9fafb;
  padding: 1rem;
  border-bottom: 1px solid #e5e7eb;
  display: flex;
  align-items: center;
  gap: 1rem;
}

.owasp-rank {
  background-color: #3b82f6;
  color: white;
  width: 2rem;
  height: 2rem;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}

.risk-level {
  margin-left: auto;
  padding: 0.25rem 0.5rem;
  border-radius: 0.25rem;
  font-size: 0.875rem;
  font-weight: 500;
}

.high-risk {
  background-color: #fee2e2;
  color: #dc2626;
}

.medium-risk {
  background-color: #fef3c7;
  color: #d97706;
}

.low-risk {
  background-color: #ecfdf5;
  color: #059669;
}

.owasp-card-body {
  padding: 1rem;
}

.owasp-card-body > * + * {
  margin-top: 1rem;
}

pre {
  background-color: #1e293b;
  color: #f8fafc;
  padding: 0.75rem;
  border-radius: 0.375rem;
  overflow-x: auto;
}

.resources a {
  color: #3b82f6;
  text-decoration: underline;
}
</style>
