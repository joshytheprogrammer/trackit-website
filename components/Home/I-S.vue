<template>
  <div class="board-component" :class="{'wide' : !mobile}">
    <div class="_image">

    </div>
    <div class="_details">
      <img src="../../assets/img/SMART.jpg" alt="">
    </div>
  </div>
</template>

<script>
import {mapGetters} from "vuex"
export default {
  computed: {
    ...mapGetters({
      mobile: 'mobile/mobile',
    })
  },
}
</script>

<style lang="scss" scoped>
.board-component {
  padding: 1rem;

  &.wide {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}
</style>