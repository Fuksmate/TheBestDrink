<template>
    <main class="row choose-drink">
        <div class="columns small-12 medium-4 medium-offset-4 choose-drink__relative">
            <img :src="drink" alt="drink">
            <div class="choose-drink__circle choose-drink__circle--left">
            </div>
            <div class="choose-drink__circle choose-drink__circle--right">
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
