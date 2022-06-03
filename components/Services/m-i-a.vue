<template>
  <div class="mia" :class="{'wide' : !mobile}">
    <div class="_details">
      <h2>Microsoft Imagine Academy</h2>
      <p>Providing the technology skills and certifications students need to succeed. Microsoft Imagine Academy gives students and educators the curricula and certifications they need to succeed in a technology-driven economy. Prepare students for college and careers with on-demand, industry-recognized courses and certifications in IT, computer science, productivity, and more. TRACK I.T. is a certified partner of Microsoft. When you finish a course with us, you get a Microsoft Certified Certificate. Come, let’s learn.</p>
      <button @click="$router.push('/quotation?interest=mia')">Subscribe</button>
    </div>
    <div class="_image" :class="{'wide' : !mobile}">
      <img src="../../assets/img/m-i-m.png" alt="ICT Lab">
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
.mia {
  height: fit-content;
  margin: 1rem 0;
  box-shadow: 0 2px 2px -2px;
  display: flex;
  flex-direction: column-reverse;

  ._image {
    max-width: 100%;
    display: flex;
    justify-content: flex-start;

    &.wide {
      justify-content: center;
    }

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
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