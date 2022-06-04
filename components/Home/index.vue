<template>
  <div class="home">
    <hero-component />
    <testimonials />
    <Maps />
    <FAQ /> 
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import Testimonials from "./testimonials.vue"
import FAQ from "./faq.vue"
import Maps from "./maps.vue"

export default {
  components: {
    HeroComponent,
    Testimonials,
    FAQ,
    Maps
  }
}
</script>

<style>

</style>