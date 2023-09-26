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
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>



<template>
    <!-- info and sites shop -->
    <div class="info-shop">
        <div class="container d-flex flex-wrap justify-content-between">

            <!-- list group -->
            <div class="eb_container-lists col-12 col-md-5 py-4">
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
            <div class=" d-none d-sm-block col-md-6 eb_logo"></div>

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
                <h2 class="pe-4 text-center text-sm-start">follow us</h2>
                <div class="logo px-2 d-flex flex-wrap gap-2">
                    <a v-for="social in socials" href="##">
                        <img :src="getImagePath(social.img)" :alt="social.name">
                    </a>
                </div>
            </div>

        </div>
    </footer>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

@use '../assets/scss/partials/footer-about-us.scss' as *;
</style>