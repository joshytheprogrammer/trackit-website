<template>
  <div class="jumbotron" :class="{'wide' : !mobile}">
    <div class="content" :class="{'wide' : !mobile}">
      <h1>We set people on right I.T. track to enable them find purpose.</h1>
      <!-- <p>We offer multiple technology solutions and certifications such as, the Microsoft Certified Educator Certification (MCE), the Microsoft Office Specialist Certification and much more. Our most popular course is the MCE certification.</p> -->
      <!-- <p></p> -->
      <a :class="{'wide' : !mobile}" href="#shop">Appy for it Now</a>
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
  text-align: center;
  justify-content: center;
  align-items: center;

  .content {
    color: $light;

    h1 {
      font-weight: 500;
    }

    h1, p {
      padding: 0.5rem 0;
    }
    
    &.wide {
      display: flex;
      justify-content: center;
      flex-direction: column;
      color: $light;
      width: 50%;

      @media screen and (max-width: 900px) {
        width: 100%;
      }

      h1 {
        font-size: 48px;
        font-weight: 400;
        line-height: 1.35;
      }

      p {
        font-size: 20px;
        line-height: 1.95;
      }

      
    }
  }

  a {
    display: block;
    background: $primary;
    color: $light;
    border: none;
    font-size: 16px;
    font-weight: 400;
    text-decoration: none;
    border-radius: 4px;
    height: fit-content;
    width: fit-content;
    padding: 8px 12px;
    margin: 1rem auto;
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