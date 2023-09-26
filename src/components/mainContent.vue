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
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>



<template>
    <div class="more">
        <div class="container d-flex flex-wrap justify-content-center">
            <div v-for="card in cards" class="col-5 col-lg  my-5">
                <img :src="getImagePath(card.image)" :alt="card.text" class="m-3">
                <span class="text-white text-uppercase ">{{ card.text }}</span>
            </div>

        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

@use '../assets/scss/partials/main-content' as *;
</style>