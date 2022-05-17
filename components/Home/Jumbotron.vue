<template>
  <div class="jumbotron" :class="{'wide' : !mobile}">
    <h1>Get a Quote</h1>
    <p>We offer multiple solutions for Schools, Teachers, Students, Individuals, and much more. These solutions include but is not limited to, 
      the Installation of Interactive Smart Board, the Installation of ICT labs in schools and businesses, Online and Offline Trainings on Technology Related Topics, Issuing of Several Microsoft Certifications and much more. If you are interested in any of these, click on the button below
    </p>
    <button @click="$router.push('/quotation')">Get Quote</button>
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
.jumbotron {
  padding: 1rem;
  max-height: 800px;
  max-width: 100%;

  &.wide {
    max-width: 50%;
  }

  display: flex;
  flex-direction: column;
  justify-content: flex-start;

  box-shadow: 0 2px 2px -2px;

  h1 {
    font-size: 28px;
  }

  p {
    font-size: 14px;
  }

  h1, p {
    padding: 0.5rem 0;
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
</style>