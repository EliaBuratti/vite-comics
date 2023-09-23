<script>
export default {
    name: 'footerAboutUs',

    data() {
        return {
            listsFooter: [
                {
                    listTitle: 'dc comics',
                    lists: [
                        { name: 'characters', link: '##' },
                        { name: 'comics', link: '##' },
                        { name: 'Movies', link: '##' },
                        { name: 'TV', link: '##' },
                        { name: 'Games', link: '##' },
                        { name: 'Videos', link: '##' },
                        { name: 'news', link: '##' },
                    ],
                },
                {
                    listTitle: 'dc',
                    lists: [
                        { name: 'therms of use', link: '##' },
                        { name: 'privacy policy (New)', link: '##' },
                        { name: 'ad choices', link: '##' },
                        { name: 'jobs', link: '##' },
                        { name: 'subscriptions', link: '##' },
                        { name: 'talent workshops', link: '##' },
                        { name: 'CPSC certificates', link: '##' },
                        { name: 'ratings', link: '##' },
                        { name: 'shop help', link: '##' },
                        { name: 'contact us', link: '##' },
                    ]
                },
                {
                    listTitle: 'sites',
                    lists: [
                        { name: 'DC', link: '##' },
                        { name: 'MAD magazine', link: '##' },
                        { name: 'DC kids', link: '##' },
                        { name: 'DC universe', link: '##' },
                        { name: 'DC power visa', link: '##' },

                    ]
                },
                {
                    listTitle: 'shop',
                    lists: [
                        { name: 'shop DC', link: '##' },
                        { name: 'shop DC collectibles', link: '##' },

                    ]
                },
            ],

            socials: [
                { name: 'facebook', img: './src/assets/img/footer-facebook.png', link: '##' },
                { name: 'twitter', img: './src/assets/img/footer-twitter.png', link: '##' },
                { name: 'youtube', img: './src/assets/img/footer-youtube.png', link: '##' },
                { name: 'pinterest', img: './src/assets/img/footer-pinterest.png', link: '##' },
                { name: 'periscope', img: './src/assets/img/footer-periscope.png', link: '##' },
            ]
        }
    }
}
</script>



<template>
    <div class="info-shop">
        <div class="container d-flex justify-content-between">
            <div class="eb_list d-flex flex-wrap col-5">
                <div v-for="(list, i) in listsFooter" class="py-4">
                    <ul class="ps-0 pe-5">

                        <li class="list-unstyled"> {{ list.listTitle }} </li>

                        <li v-for="object in list.lists" class="list-unstyled">

                            <a :href="object.link" class="text-decoration-none">
                                {{ object.name }}
                            </a>
                        </li>
                        <li class="list-unstyled">

                        </li>
                    </ul>
                </div>
            </div>
            <div class="col-6 eb_logo"></div>
        </div>
    </div>
    <footer>
        <div class="container d-flex justify-content-between py-4 align-items-center">

            <div class="register">
                <button>sing-up now!</button>
            </div>

            <div class="social d-flex">
                <h2 class="pe-4">follow us</h2>
                <div v-for="social in socials" class="logo px-2">
                    <a href="##">
                        <img :src="social.img" :alt="social.name">
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;


.info-shop {
    width: 100%;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;

    .eb_logo {
        background: url(../assets/img/dc-logo-bg.png) right no-repeat;
    }

}

ul>li:first-child {
    font-size: 1.3rem;
    font-weight: bold;
    text-transform: uppercase;
    color: $white-color;

}

ul>li {
    text-transform: capitalize;
    font-size: 0.9rem;

    a {
        color: $list-color;
    }
}

footer {
    background-color: $bg-footer;

    .register button {
        background-color: transparent;
        border: 2px solid $primary-color;
        color: $white-color;
        padding: 1rem;
        text-transform: uppercase;
        font-weight: bold;
    }

    .social {

        h2 {
            color: $primary-color ;
            text-transform: uppercase;
            font-weight: bold;
        }
    }

}
</style>