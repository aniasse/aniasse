<script setup lang="ts">
defineProps<{
  title: string
  content: string
}>()
</script>

<template>
  <details class="mb-6 group">
    <summary class="flex items-center cursor-pointer text-accent-600 font-bold text-lg">
      <span>{{ title }}</span>
      <Icon 
        name="material-symbols:keyboard-arrow-down" 
        class="ml-2 transform group-open:rotate-180 transition-transform"
      />
    </summary>
    <div class="mt-4 prose prose-slate max-w-none" v-html="content"></div>
  </details>
</template>
