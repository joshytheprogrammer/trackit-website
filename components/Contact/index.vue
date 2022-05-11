<template>
  <section class="contact" :class="{'wide' : !mobile}">
    <info-cards />
    <contact-form />
  </section>
</template>

<script>
import {mapGetters} from "vuex"
import ContactForm from "./Form.vue"
import InfoCards from "./Info.vue"
export default {
  computed: {
    ...mapGetters({
      mobile: 'mobile/mobile',
    })
  },
  components: {
    ContactForm,
    InfoCards
  }
}
</script>

<style lang="scss" scoped>
.contact {
  display: block;

  &.wide {
    display: grid;
    grid-template-columns: 1fr 2fr;
    padding: 1rem;
  }
}
</style>