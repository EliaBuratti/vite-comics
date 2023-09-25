<script>
import comicCard from './comicCard.vue';
import dcComicsThumb from '../dataJs/dcComicsThumb';

export default {

    name: 'card',

    components: {
        dcComicsThumb,
        comicCard,
    },

    data() {
        return {
            thumbsCard: dcComicsThumb,
        }
    },

}
</script>
<template>
    <div class="eb_jumbotron">

        <div class=" eb_cards p-5">
            <div class="container d-flex flex-wrap gap-4 justify-content-center">
                <comicCard v-for="thumb in thumbsCard" :thumb="thumb.thumb" :price="thumb.price" :series="thumb.series"
                    :type="thumb.type" />
            </div>

            <button class="load_more">LOAD MORE</button>
        </div>

    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.eb_jumbotron {
    background-image: url(../assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: 100%;
    padding-top: 20%;

    &::before {
        content: 'CURRENT SERIES';
        font-weight: bold;
        font-size: 1.6rem;
        padding: 1rem 3rem;
        background-color: $primary-color;
        color: $white-color;
        margin-left: 15%;
    }

    .eb_cards {
        background-color: $bg-thumb-card;

        .load_more {
            margin-left: 50%;
            transform: translate(-50%);
            color: $white-color;
            background-color: $primary-color;
            border: none;
            padding: 0.5rem 3rem;
        }

    }

}
</style>