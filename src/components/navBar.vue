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
    <div class="container px-0">
        <nav class="navbar navbar-expand-lg">
            <div class="container">
                <a class="navbar-brand eb_logo" href="#">
                    <img src="../assets/img/dc-logo.png" alt="Logo" width="30" height="30"
                        class="d-inline-block align-text-top">
                </a>
            </div>
            <div class="eb_nav-section">
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                    aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav">
                        <li v-for="section in navSections" class="nav-item text-uppercase font-weight-bold">
                            <a class="nav-link active" aria-current="page" href="#">{{ section }}</a>
                        </li>
                    </ul>
                </div>

            </div>
        </nav>
    </div>
</template>


<style lang="scss" scoped>
.eb_logo img {
    width: 5rem;
    height: 5rem;
}
</style>