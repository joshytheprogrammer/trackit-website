<template>
  <div class="menuItems" :class="{'wide' : !mobile}">
    <div class="links" :class="{'wide' : !mobile}">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/services">Services</NuxtLink>
      <NuxtLink to="/about">About</NuxtLink>
      <NuxtLink to="/contact">Contact</NuxtLink>
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

      font-weight: 500;
      font-size: 16px;

      padding: 9px 0;

      &:hover {
        color: $primary;
      }

      &.nuxt-link-active {
        font-weight: 700;
        color: $dark;
      }

      &.nuxt-link-exact-active {
        font-weight: 700;
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
        filter: brightness(110%);
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