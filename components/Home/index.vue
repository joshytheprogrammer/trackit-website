<template>
  <div class="home">
    <hero-component />
    <Shop />
    <testimonials /> 
    <Maps />
    <FAQ /> 
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import Shop from "./Shop.vue"
import Testimonials from "./testimonials.vue"
import FAQ from "./faq.vue"
import Maps from "./maps.vue"

export default {
  components: {
    HeroComponent,
    Shop,
    Testimonials,
    FAQ,
    Maps
  }
}
</script>

<style>

</style>