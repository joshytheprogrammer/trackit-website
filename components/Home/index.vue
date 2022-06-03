<template>
  <div class="home">
    <hero-component />
    <testimonials />
    <FAQ /> 
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import Testimonials from "./testimonials.vue"
import FAQ from "./faq.vue"

export default {
  components: {
    HeroComponent,
    Testimonials,
    FAQ
  }
}
</script>

<style>

</style>