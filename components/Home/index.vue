<template>
  <div class="home">
    <hero-component />
    <board-component />
    <MCE />
    <Lab />
    <MIA />
    <FAQ /> 
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import BoardComponent from "./I-S.vue"
import MCE from "./M-C-E.vue"
import Lab from "./ict-lab.vue"
import MIA from "./m-i-a.vue"
import FAQ from "./faq.vue"

export default {
  components: {
    HeroComponent,
    BoardComponent,
    MCE,
    Lab,
    MIA,
    FAQ
  }
}
</script>

<style>

</style>