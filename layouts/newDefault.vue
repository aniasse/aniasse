<template>
  <div>
    <LayoutsPageNavbar />
    <slot />
    <LayoutsPageNewFooter />
  </div>
</template>

<script setup>
import LayoutsPageNavbar from '@/components/layouts/Page/Navbar.vue'
import LayoutsPageNewFooter from '@/components/layouts/Page/NewFooter.vue'
</script>
