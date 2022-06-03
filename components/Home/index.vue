<template>
  <div class="home">
    <hero-component />
    <FAQ /> 
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import FAQ from "./faq.vue"

export default {
  components: {
    HeroComponent,
    FAQ
  }
}
</script>

<style>

</style>