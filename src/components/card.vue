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

    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }

}
</script>
<template>
    <div class="eb_jumbotron">
        <img :src="getImagePath('jumbotron.jpg')" alt="jumbotron">




        <div class=" eb_cards p-5">
            <div class="container d-flex flex-wrap gap-5 justify-content-center">
                <h3>current series</h3>
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



    img {
        width: 100%;
        height: 15rem;
        object-fit: cover;
        object-position: top center;

    }

    h3 {
        text-transform: uppercase;
        width: fit-content;
        font-weight: bold;
        font-size: 1.6rem;
        padding: 1rem 3rem;
        background-color: $primary-color;
        color: $white-color;
        position: absolute;
        top: -5rem;
        left: 0;
    }


    /*     &::before {
        content: 'CURRENT SERIES';
        font-weight: bold;
        font-size: 1.6rem;
        padding: 1rem 3rem;
        background-color: $primary-color;
        color: $white-color;
        margin-left: 15%;
    } */

    /*     background-image: url(../assets/img/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: 100%;
    padding-top: 20%; */


    .eb_cards {
        background-color: $bg-thumb-card;

        >div {
            position: relative;
        }

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