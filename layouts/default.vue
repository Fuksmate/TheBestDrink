<template>
  <div>
    <TheHeader />
    <Nuxt />
  </div>
</template>
<script>
import TheHeader from '~/components/TheHeader.vue'

export default {
  name: 'Layout',
  components: {
    TheHeader
  }
}
</script>
<style lang="scss">
</style>
