<script>
export default {
    name: 'mainContent',

    data() {

        return {

            cards: [
                {
                    text: 'digital comics',
                    image: 'buy-comics-digital-comics.png', // persorso da sistemare!!!
                },
            ]
        }
    }
}
</script>



<template>
    <div class="aboutUs">
        <div class="container d-flex">
            <!--             <div class="col">
                <img src="../assets/img/buy-comics-digital-comics.png" alt="digital">
                <span class="text-white text-uppercase">digital comics</span>
            </div> -->

            <div v-for="card in cards" class="col">
                <img :src="card.image" alt="digital">
                <span class="text-white text-uppercase">{{ card.text }}</span>
            </div>

        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.aboutUs {
    background-color: $primary-color;
}
</style>