<template>
  <div class="container">
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const response = await $axios.$get('/random.php')
    console.log(response);
    return {
      page: response
    }
  }
}
</script>

<style lang="scss">

</style>
