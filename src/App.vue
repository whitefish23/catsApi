<template>
  <HeaderPage />
  <RouterView />
  <FooterPage />
  
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import FooterPage from '@/components/FooterPage.vue';

export default {
    components: {
      HeaderPage, FooterPage
    },
  }
</script>

<style lang="scss">
</style>