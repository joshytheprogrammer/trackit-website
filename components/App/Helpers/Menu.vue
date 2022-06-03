<template>
  <div class="menuItems" :class="{'wide' : !mobile}">
    <div class="links" :class="{'wide' : !mobile}">
      <NuxtLink to="/">Home</NuxtLink>
      <!-- <NuxtLink to="/services">Services</NuxtLink> -->
      <NuxtLink to="/about">About</NuxtLink>
      <NuxtLink to="/contact-us">Contact</NuxtLink>
      <button @click="$router.push('/quotation')">Get a Quote</button>
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
.menuItems {
  padding: 9px;

  &.wide {
    padding: 6px 0;
  }

  .links {
    display: flex;
    flex-direction: column;
    
    a {
      text-decoration: none;
      color: $dark;
      cursor: pointer;

      font-weight: 400;
      font-size: 16px;

      padding: 9px 0;

      &:hover {
        text-decoration: underline;
        text-underline-offset: 7px; 
      }

      &.nuxt-link-exact-active {
        text-decoration: underline;
        text-underline-offset: 7px; 
        color: $dark;
      }
    }

    button {
      background: $primary;
      border: none;
      padding: 8px;
      color: $light;
      border-radius: 4px;
      font-weight: 600;
      width: fit-content;
      cursor: pointer;

      &:hover {
        box-shadow: 0px 8px 8px $grey;
      }
    }

    &.wide {
      flex-direction: row;
      align-items: center;

      a {
        padding: 0 9px;
      }
    }
  }
}
</style>