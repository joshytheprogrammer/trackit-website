<template>
  <div class="home">
    <hero-component />
    <board-component />
    <mce />
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import BoardComponent from "./I-S.vue"
import MCE from "./M-C-E.vue"
export default {
  components: {
    HeroComponent,
    BoardComponent,
    MCE
  }
}
</script>

<style>

</style>