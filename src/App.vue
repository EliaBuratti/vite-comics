<script>
import navBar from './components/navBar.vue';
import mainContent from './components/mainContent.vue';
import footerAboutUs from './components/footerAboutUs.vue';

export default {

  name: 'app',
  data() {
    return {

    }
  },
  components: { // da inserire tutti gli import che faccio
    navBar,
    mainContent,
    footerAboutUs,
  }

}

</script>

<template>
  <navBar></navBar>
  <mainContent></mainContent>
  <footerAboutUs></footerAboutUs>
</template>

<style lang="scss" scoped>
@use './assets/scss/partials/variables' as *;
</style>

