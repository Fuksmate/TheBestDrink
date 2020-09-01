<template>
  <div class="container">
      <ChooseDrink :drink="drink" />
  </div>
</template>

<script>
import ChooseDrink from '~/components/ChooseDrink'

export default {
  name: 'index',
  components: {
    ChooseDrink
  },
  async asyncData({ $axios }) {
  const response = await $axios.$get('/random.php')
    return {
      drink: response.drinks[0].strDrinkThumb
    }
  }
}
</script>

<style lang="scss">

</style>
