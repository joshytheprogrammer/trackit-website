<template>
  <div class="our-story" :class="{'wide' : !mobile}">
    <div class="_details">
      <h1>The Company <br> TrackIT</h1>
      <p><bold>TrackIT</bold> was founded in 2014 for the sole purpose of setting people on the right IT track to enable them find their place in the booming tech industry. Fast forward a few years and now <bold>TrackIT</bold> has trained over 50,000 students, and certified thousands more. We have setup hundreds of ICT labs around the world and are gradually ramping up our installtions of the <bold>Interactive Smart Board.</bold></p>
    </div>
    <div class="_image">
      <img src="https://images.unsplash.com/photo-1602763288580-927cfda37a72?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2072&q=80" alt="trackit-image-2">
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
.our-story {
  padding: 2rem 1rem;

  &.wide {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  ._details {
    width: 40%;
    line-height: 1.7;

    h1 {
      padding: 0.5rem 0;
      font-size: 36px;
      font-weight: 500;
    }

    p {
      font-weight: 400;
      font-size: 14px;

      bold {
        font-weight: 500;
      }
    }
  }

  ._image {
    max-width: 50%;

    img {
      width: 100%;
      height: 100%;
      object-fit: fill;
    }
  }
}
</style>