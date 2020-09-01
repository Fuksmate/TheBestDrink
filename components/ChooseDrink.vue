<template>
    <main class="row choose-drink">
        <div class="columns small-12 medium-4 medium-offset-4">
            <img :src="drink" alt="drink">
            <div class="fullwidth">
           
            </div>
        </div>
    </main>
</template>

<script>
export default {
    name: 'ChooseDrink',
    props: {
        drink: {
            type: String,
            required: true,
        }
    }
}
</script>

<style lang="scss">
.choose-drink {
    padding-top: 20px;
}
</style>
