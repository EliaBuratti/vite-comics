<script>
export default {
    name: 'mainContent',

    data() {

        return {

            cards: [
                {
                    text: 'digital comics',
                    image: './src/assets/img/buy-comics-digital-comics.png',
                },
                {
                    text: 'digital comics',
                    image: './src/assets/img/buy-comics-merchandise.png',
                },
                {
                    text: 'digital comics',
                    image: './src/assets/img/buy-comics-subscriptions.png',
                },
                {
                    text: 'digital comics',
                    image: './src/assets/img/buy-comics-shop-locator.png',
                },
                {
                    text: 'digital comics',
                    image: './src/assets/img/buy-dc-power-visa.svg',
                },
            ]
        }
    }
}
</script>



<template>
    <div class="more_content">
        <div class="container p-3">
            <h2>Content goes here</h2>
        </div>
    </div>
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

.more {
    background-color: $primary-color;

    & img {
        height: 3.5rem;
    }

    & span {
        font-size: 1rem;
    }
}

.more_content {
    height: 8rem;
    background-color: $black-color;
    color: $white-color;
}
</style>