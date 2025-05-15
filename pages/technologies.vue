<!-- eslint-disable -->
<template>
  <div class="container mx-auto px-4 py-8">
    <h1 class="text-3xl font-bold mb-6">Technical Expertise</h1>
    <div class="space-y-8">
      <section>
        <h2 class="text-2xl font-semibold mb-4">Web Development</h2>
        <p>Modern web technologies and frameworks.</p>
      </section>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: 'TechnologiesPage',
  head() {
    return {
      title: 'Technical Expertise',
      meta: [
        { hid: 'description', name: 'description', content: 'My technical skills and experience' }
      ]
    }
  }
}
</script>

<style scoped>
.container {
  max-width: 1200px;
}
</style>
