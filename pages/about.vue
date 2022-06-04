<template>
  <div class="about" :class="{'wide' : !mobile}">
    <OS />
    <section class="old">
      <WWA />
      <ISC />
    </section>
    <section class="btn">
      <button @click="$router.push('/quotation')">Get a Quote</button>
    </section>
  </div>
</template>

<script>
import {mapGetters} from "vuex"
import WWA from "~/components/About/w-w-a.vue"
import ISC from "~/components/About/i-s-c.vue"
import OS from "~/components/About/o-s.vue"

export default {
  computed: {
    ...mapGetters({
      mobile: 'mobile/mobile',
    })
  },
  components: {
    WWA,
    ISC,
    OS
  }
}
</script>

<style lang="scss" scoped>
.about {
  &.wide {
    .old {
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
  }

  .old {
    display: block;
  }

  .btn {
    display: flex;
    justify-content: center;

    button {
      background: $primary;
      color: $light;
      border: none;
      font-size: 16px;
      font-weight: 400;
      border-radius: 4px;
      height: fit-content;
      width: fit-content;
      padding: 8px 12px;
      margin: 1rem 0;
      cursor: pointer;
      transition: box-shadow .2s ease-in-out;

      &:hover {
        box-shadow: 0px 8px 8px $dark;
      }
    }
  }
}
</style>