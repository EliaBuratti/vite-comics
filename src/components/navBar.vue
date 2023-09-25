<script>
export default {
    name: 'navBar',

    data() {

        return {

            navSections: ['characters', 'comics', 'movies', 'tv', 'games', 'collectibles', 'videos', 'fans', 'news', 'shop'],
        }
    }
}
</script>



<template>
    <div class="container px-0 pt-2">
        <nav class="navbar navbar-expand-lg p-0">
            <a class="navbar-brand eb_logo" href="#">
                <img src="../assets/img/dc-logo.png" alt="Logo" width="30" height="30"
                    class="d-inline-block align-text-top">
            </a>

            <div class="ms-auto eb_nav-section">
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                    aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav ">
                        <li v-for="section in navSections" class="nav-item text-uppercase eb_nav-section">
                            <a class="nav-link active" aria-current="page" href="#">{{ section }}</a>
                        </li>
                    </ul>
                </div>

            </div>
        </nav>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

@use '../assets/scss/partials/nav-bar' as *;
</style>