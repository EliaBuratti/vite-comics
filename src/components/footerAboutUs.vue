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
                    ]
                },
                {
                    listTitle: 'dc comics',
                    lists: [
                        { name: 'Characters', link: '##' },
                        { name: 'Comics', link: '##' },
                        { name: 'Movies', link: '##' },
                        { name: 'TV', link: '##' },
                        { name: 'Games', link: '##' },
                        { name: 'Videos', link: '##' },
                        { name: 'News', link: '##' },
                    ]
                },
                {
                    listTitle: 'dc comics',
                    lists: [
                        { name: 'Characters', link: '##' },
                        { name: 'Comics', link: '##' },
                        { name: 'Movies', link: '##' },
                        { name: 'TV', link: '##' },
                        { name: 'Games', link: '##' },
                        { name: 'Videos', link: '##' },
                        { name: 'News', link: '##' },
                    ]
                },
                {
                    listTitle: 'dc comics',
                    lists: [
                        { name: 'Characters', link: '##' },
                        { name: 'Comics', link: '##' },
                        { name: 'Movies', link: '##' },
                        { name: 'TV', link: '##' },
                        { name: 'Games', link: '##' },
                        { name: 'Videos', link: '##' },
                        { name: 'News', link: '##' },
                    ]
                },
                {
                    listTitle: 'dc comics',
                    lists: [
                        { name: 'Characters', link: '##' },
                        { name: 'Comics', link: '##' },
                        { name: 'Movies', link: '##' },
                        { name: 'TV', link: '##' },
                        { name: 'Games', link: '##' },
                        { name: 'Videos', link: '##' },
                        { name: 'News', link: '##' },
                    ]
                },
            ],
        }
    }
}
</script>



<template>
    <div class="info-shop">

        <div class="container d-flex justify-content-between">
            <div class="col-5 d-flex flex-wrap py-4">
                <ul v-for="list in listsFooter" class="ps-0 pe-5">
                    <li v-for="object in list.lists" class="list-unstyled">
                        <a :href="object.link" class="text-decoration-none">
                            {{ object.name }}
                        </a>
                    </li>
                </ul>
            </div>
            <div class="col-6 eb_logo"></div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;


.info-shop {
    width: 100%;
    background: url(../assets/img/footer-bg.jpg);
    object-fit: cover;

    & .eb_logo {
        background: url(../assets/img/dc-logo-bg.png) center no-repeat;
    }

}

ul>li:first-child {
    font-weight: bold;
    text-transform: uppercase;

    & a {
        color: $white-color;
    }
}

ul>li {
    text-transform: capitalize;

    & a {
        color: $list-color;
    }
}
</style>