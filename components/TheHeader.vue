<template>
  <header class="row header">
    <div class="columns small-12 text-center header__logo">
        This is the database of the best drinks of all time
    </div>
    <div class="columns small-12 header__beam">
      <nav class="columns large-8 large-offset-3 text">
            <ul>
                <li><nuxt-link to="/about">Home</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
                <li><nuxt-link to="/about">RNG Drink</nuxt-link></li>
                <li><nuxt-link to="/about">Top 10</nuxt-link></li>
            </ul>
      </nav> 
    </div>
  </header>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style lang="scss">
.header {
    &__logo{
        height: 5vh;
        background-color: #F2E9E1;
        font-size:22px
    }
    &__beam{
        background-color: #CBE86B;
        height: 10vh;
        position: relative;
        ul {
            list-style-type: none;
            position: absolute;
            top:50%;
            transform: translate(0, -50%);
            li {
                display: block;
                float: left;
                text-align: center;
                font-size:17px;
                font-weight: 200;
                width: 230px;
            }
        }
    }
}
</style>
