<template>
  <div class="home">
    <hero-component />
    <Vouchers />
    <Shop />
    <Antivirus />
    <Offerings />
    <!-- <testimonials />  -->
    <Maps />
    <FAQ /> 
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import Antivirus from "./antivirus.vue"
import Vouchers from "./vouchers.vue"
import Shop from "./Shop.vue"
import Offerings from "./offerings.vue"
import Testimonials from "./testimonials.vue"
import FAQ from "./faq.vue"
import Maps from "./maps.vue"

export default {
  components: {
    HeroComponent,
    Antivirus,
    Shop,
    Vouchers,
    Offerings,
    Testimonials,
    FAQ,
    Maps
  }
}
</script>

<style>

</style>