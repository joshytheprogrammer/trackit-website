<template>
  <div class="home">
    <hero-component />
    <Shop />
    <Offerings />
    <testimonials /> 
    <Maps />
    <FAQ /> 
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import Shop from "./Shop.vue"
import Offerings from "./offerings.vue"
import Testimonials from "./testimonials.vue"
import FAQ from "./faq.vue"
import Maps from "./maps.vue"

export default {
  components: {
    HeroComponent,
    Shop,
    Offerings,
    Testimonials,
    FAQ,
    Maps
  }
}
</script>

<style>

</style>