<script>
export default {
    name: 'comicCard',

    props: {
        thumb: String,
        price: String,
        series: String,
        type: String,
    },


}
</script>


<template>
    <div class="eb_card">
        <img :src="thumb" :alt="series">
        <p>{{ series }}</p>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.eb_card {
    width: 12rem;
    color: $white-color;
    text-transform: uppercase;
    word-wrap: break-word;

    img {
        width: 12rem;
        aspect-ratio: 1 / 1;
        object-fit: cover;
    }
}
</style>






