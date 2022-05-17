<template>
  <div class="home">
    <hero-component />
    <board-component />
    <MCE />
    <Lab />
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import BoardComponent from "./I-S.vue"
import MCE from "./M-C-E.vue"
import Lab from "./ict-lab.vue"
export default {
  components: {
    HeroComponent,
    BoardComponent,
    MCE,
    Lab
  }
}
</script>

<style>

</style>