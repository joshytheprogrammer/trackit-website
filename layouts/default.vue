<template>
  <div class="app">
    <Navigation />
    <Nuxt />
    <!-- <Footer /> -->
  </div>
</template>

<script>
import Navigation from "../components/App/NavBar.vue"
import Footer from "../components/App/Footer.vue"
export default {
  components: {
    Navigation,
    Footer
  }
}
</script>

<style lang="scss" scoped>
.app {
  display: flex;
  flex-direction: column;
}
</style>