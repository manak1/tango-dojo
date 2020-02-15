<template>
  <main>
    <l-header />
    <nuxt />
  </main>
</template>
<script>
import LHeader from '@/components/layout/Header'
export default {
  components: { LHeader }
}
</script>

<style lang="scss">
html,
body {
  font-size: 62.5%;
  margin: 0;
}
</style>
