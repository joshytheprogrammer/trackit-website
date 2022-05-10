<template>
  <div class="app">
      <Navigation />
      <section >
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
section {
  min-height: 100vh;
}
</style>