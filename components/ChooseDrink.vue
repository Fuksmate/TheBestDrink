<template>
    <main class="row choose-drink">
        <div class="columns small-12 medium-4 medium-offset-4 choose-drink__relative">
            <img :src="mountains.drinks[0].strDrinkThumb" alt="drink">
            <div @click="$fetch" class="choose-drink__circle choose-drink__circle--left">
            </div>
            <div @click="$fetch" class="choose-drink__circle choose-drink__circle--right">
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'ChooseDrink',
    data() {
      return {
        mountains: ''
      }
    },
    async fetch() {
      this.mountains = await fetch(
      'https://www.thecocktaildb.com/api/json/v1/1/random.php'
      ).then(res => res.json())
    },
}
</script>

<style lang="scss">
.choose-drink {
    padding-top: 20px;
    &__relative {
        position: relative;
    }
    &__circle {
        border-radius: 50%;
        width: 125px;
        height: 125px;
        &--left {
            position: absolute;
            background-color: red;
            bottom: 0;
            left: 18px;
        }
        &--right {
            position: absolute;
            background-color: greenyellow;
            bottom: 0;
            right: 18px;
        }
    }
}
</style>
