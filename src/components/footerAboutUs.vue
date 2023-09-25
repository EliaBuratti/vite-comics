<script>
import socials from "../dataJs/socials.js";
import listsInfo from "../dataJs/listsInfo.js";

export default {
    name: 'footerAboutUs',

    components: {
        socials,
        listsInfo,
    },

    data() {
        return {
            socials: socials,
            listsInfo: listsInfo,
        }
    },
}
</script>



<template>
    <!-- info and sites shop -->
    <div class="info-shop">
        <div class="container d-flex justify-content-between">

            <!-- list group -->
            <div class="eb_container-lists col-5 py-4">
                <!-- single list -->
                <ul v-for="list in listsInfo" class="eb_list ps-0 pb-2">
                    <li class="list-unstyled"> {{ list.listTitle }} </li>
                    <li v-for="object in list.lists" class="list-unstyled">
                        <a :href="object.link" class="text-decoration-none">
                            {{ object.name }}
                        </a>
                    </li>
                </ul>
            </div>

            <!-- logo -->
            <div class="col-6 eb_logo"></div>

        </div>
    </div>

    <!-- site footer -->
    <footer>

        <!-- footer bar -->
        <div class="container d-flex justify-content-between py-4 align-items-center">

            <!-- register button -->
            <div class="register">
                <button>sing-up now!</button>
            </div>

            <!-- socials -->
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

    .eb_container-lists {
        column-count: 3;
        column-gap: 1rem;
    }

    /* mansory layout */
    .eb_list {
        margin: 0;
        display: grid;
        grid-template-rows: auto auto;
        break-inside: avoid;
    }

    /* end mansory layout */

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