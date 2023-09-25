<script>
import cards from '../dataJs/cards.js'
export default {
    name: 'mainContent',

    components: {
        cards,
    },
    data() {

        return {
            cards: cards.cards,
        }
    }
}
</script>



<template>
    <div class="more">
        <div class="container d-flex">
            <div v-for="card in cards" class="col my-5">
                <img :src="card.image" :alt="card.text" class="m-3">
                <span class="text-white text-uppercase">{{ card.text }}</span>
            </div>

        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

@use '../assets/scss/partials/main-content' as *;
</style>