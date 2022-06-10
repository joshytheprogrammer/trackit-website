<template>
  <div class="quotation" :class="{'wide' : !mobile}">
    <Form />
    <div class="image" v-if="!mobile">
      <img src="../../assets/img/quotation-right-image.jpg" alt="">
    </div>
  </div>
</template>

<script>
import {mapGetters} from "vuex"
import Form from "./Form.vue"

export default {
  computed: {
    ...mapGetters({
      mobile: 'mobile/mobile',
    })
  },
  components: {
    Form
  }
}
</script>

<style lang="scss" scoped>
.quotation {
  &.wide {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .image {
    max-height: 700px;
    
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
}
</style>