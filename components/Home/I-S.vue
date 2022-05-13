<template>
  <div class="board-component" :class="{'wide' : !mobile}">
    <div class="_image">
      <img src="../../assets/img/SMART.jpg" alt="The Interactive Smart Board">
    </div>
    <div class="_details">
      <h2>The Interactive Smartboard</h2>
      <p>Track I.T installs Smart Boards in schools and businesses. We use the most efficient and cost effective methods of Installation to ensure that the boards last as long as possible while also serving its purpose. We have installed over a hundred Smartboard in schools and offices all around Nigeria</p>
      <button>Learn More</button>
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
  margin: 0.5rem 0;
  box-shadow: 0 2px 2px -2px;

  ._image {
    max-width: 100%;
    max-height: 450px;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  ._details {
    padding: 1rem;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;

    h2 {
      font-size: 24px;
      font-weight: 500;
      padding-bottom: 1rem;
    }

    p {
      font-weight: 400;
      font-size: 14px;
    }
  }

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
    transition: box-shadow .2s ease-in-out, padding .2s linear;

    &:hover {
      box-shadow: 0px 8px 8px $dark;
    }
  }

  &.wide {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}
</style>