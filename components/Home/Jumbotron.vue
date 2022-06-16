<template>
  <div class="jumbotron" :class="{'wide' : !mobile}">
    <div class="content" :class="{'wide' : !mobile}">
      <h1>We are committed to helping you in every way</h1>
      <p>We offer multiple solutions for Schools, Teachers, Students, Individuals, and much more. These solutions include but is not limited to, 
        the Installation of Interactive Smart Board, the Installation of ICT labs in schools and businesses, Online and Offline Trainings on Technology Related Topics, Issuing of Several Microsoft Certifications and much more. If you are interested in any of these, click on the button below
      </p>
      <button :class="{'wide' : !mobile}" @click="$router.push('/quotation')">Get a Quote</button>
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
.jumbotron {
  padding: 1rem;
  max-height: 800px;
  max-width: 100%;

  background-image: url('https://images.unsplash.com/photo-1648737155328-0c0012cf2f20?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1200&q=80');
  background-color: $dark;
  padding-bottom: 2rem;
  height: 600px;

  &.wide {
    background-image: url("https://images.unsplash.com/photo-1648737155328-0c0012cf2f20?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1700&q=80");
    background-attachment: fixed;
    background-repeat: no-repeat;
    object-fit: fill;
    height: 1500px;
    max-width: 100%;
  }

  display: flex;
  align-items: center;

  .content {
    color: $light;
    h1 {
      font-weight: 400;
    }

    h1, p {
      padding: 0.5rem 0;
    }
    
    &.wide {
      display: flex;
      flex-direction: column;
      color: $light;
      width: 50%;

      @media screen and (max-width: 900px) {
        width: 100%;
      }

      h1 {
        font-size: 36px;
        font-weight: 400;
        line-height: 1.35;
      }

      p {
        font-size: 14px;
        line-height: 1.95;
      }

      
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
    transition: background .2s ease-in-out, color .2s linear;

    &:hover {
      background: $primary;
      color: $light;
    }

    &.wide {
      background: $light;
      color: $dark;

      &:hover {
        background: $primary;
        color: $light;
      }
    }
  }
}
</style>