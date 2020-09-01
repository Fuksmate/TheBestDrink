<template>
    <main class="row chose-drink">
        {{ drink }}
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
</style>
