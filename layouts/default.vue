<template>
  <div class="app">
      <Navigation />
      <section >
        <!-- style="min-height: 100vh;" -->
        <Nuxt />
      </section>
      <Footer />
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

<style>

</style>