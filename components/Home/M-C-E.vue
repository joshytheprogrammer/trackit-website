<template>
  <div class="mce" :class="{'wide' : !mobile}">
    <div class="_details">
      <h2>Microsoft Certified Educator</h2>
      <p>The Microsoft Certified Educator (MCE) certification validates that educators have the global educator technology literacy competencies needed to provide a rich, custom learning experience for students. MCE certification is ideal for educators-in-training, faculty of teacher training colleges, and in-service educators. Tract I.T. prepares you to obtain the certificate as well as delivers the certificate when you pass.</p>
      <button @click="$router.push('/quotation?interest=mce')">Register Now</button>
    </div>
    <div class="_image" :class="{'wide' : !mobile}">
      <img src="../../assets/img/m-c-e.svg" alt="Microsoft Certified Educator">
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
.mce {
  height: fit-content;
  margin: 0.5rem 0 0 0;
  box-shadow: 0 2px 2px -2px;
  display: flex;
  flex-direction: column-reverse;

  ._image {
    max-width: 100%;
    display: flex;
    justify-content: flex-start;

    &.wide {
      border: 1px dotted $dark;
      justify-content: center;
    }

    img {
      width: 70%;
      height: 90%;
    }
  }

  &.wide {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  ._details {
    padding: 1rem;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;

    h2 {
      font-size: 36px;
      font-weight: 500;
      padding-bottom: 1rem;
    }

    p {
      font-weight: 400;
      font-size: 14px;
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
    
  }

  
}
</style>