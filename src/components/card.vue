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
    <comicCard v-for="thumb in thumbsCard" :thumb="thumb.thumb" :price="thumb.price" :series="thumb.series"
        :type="thumb.type" />
</template>


<style lang="scss" scoped></style>