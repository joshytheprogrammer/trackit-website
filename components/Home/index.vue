<template>
  <div class="home">
    <hero-component />
    <board-component />
  </div>
</template>

<script>
import HeroComponent from "./Jumbotron.vue"
import BoardComponent from "./I-S.vue"
export default {
  components: {
    HeroComponent,
    BoardComponent
  }
}
</script>

<style>

</style>