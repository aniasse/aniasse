<template>
  <div class="case-study">
    <div class="case-study-header">
      <h3>{{ title }}</h3>
      <span class="impact-badge">Impact: {{ impact }}</span>
    </div>
    <div class="case-study-content">
      <slot></slot>
      <div class="lesson">
        <strong>Leçon :</strong> {{ lesson }}
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  impact: {
    type: String,
    required: true  
  },
  lesson: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
.case-study {
  border-left: 4px solid #ef4444;
  padding-left: 1rem;
  margin-bottom: 2rem;
}

.case-study-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 0.5rem;
}

.impact-badge {
  background-color: #fef2f2;
  color: #dc2626;
  padding: 0.25rem 0.5rem;
  border-radius: 0.25rem;
  font-size: 0.875rem;
  font-weight: 500;
}

.lesson {
  margin-top: 1rem;
  padding: 0.75rem;
  background-color: #f0fdf4;
  border-left: 3px solid #10b981;
}
</style>
