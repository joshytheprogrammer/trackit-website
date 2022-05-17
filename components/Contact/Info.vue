<template>
  <div class="info" :class="{'wide' : !mobile}">
    <div class="card" :class="{'wide' : !mobile}">
      <div class="property">
        <span class="key">Address1:</span>
        <span class="value">79, Sanya Street, Aguda, Surulere, Lagos</span>
      </div>
      <div class="property">
        <span class="key">Address2:</span>
        <span class="value">84, Adetola Street, Aguda, Surulere, Lagos</span>
      </div>
    </div>
    <div class="card" :class="{'wide' : !mobile}">
      <div class="property">
        <span class="key">FaceBook:</span>
        <span class="value">@trackit-ng</span>
      </div>
      <div class="property">
        <span class="key">Instagram</span>
        <span class="value">@trackit-ng</span>
      </div>
    </div>
    <div class="card" :class="{'wide' : !mobile}">
      <div class="property">
        <span class="key">Reach us on:</span>
        <span class="value"> +234 802 317 8729 | +234 901 563 0453</span>
      </div>
      <div class="property">
        <span class="key">Email us at:</span>
        <span class="value">info@trackit.com.ng</span>
      </div>
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
.info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  &.wide {
    justify-content: flex-start;
    padding: 1rem;
  }

  .card {
    background: $light;
    border: 1px solid $dark;
    width: 95%;
    height: fit-content;
    padding: 3rem 1rem;
    margin: 1rem 0;
    border-radius: 5px;
    box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.25), 0px 2px 2px rgba(0, 0, 0, 0.25), 0px 2px 2px rgba(0, 0, 0, 0.25);

    &.wide {
      margin: 1rem 0;
    }

    .property {
      font-size: 14px;

      .key {
        font-weight: 500;
      }

      .value {
        font-weight: 300
      }
    }
  }
}
</style>