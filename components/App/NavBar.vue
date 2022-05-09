<template>
  <nav :class="{ active: isOpen }">
    <div class="navItems">
      <div class="logo">
        <img src="../../assets/img/trackit_logo.jpeg" alt="Track I.T. Logo">
      </div>
      <!-- If the screen is small show MenuIcon -->
      <div class="menuIcon" v-if="mobile">
        <MenuIcon @click="toggleMenu" />
      </div>
      <!-- Else Show menuLinks -->
      <template class="menuLinks" v-else>
        <Menu />
      </template>
    </div>
    <!-- If screen is small and menu is open show menu -->
    <div class="menu" v-if="isOpen && mobile">
      <Menu />
    </div>
  </nav>
</template>

<script>
import Menu from "./Helpers/Menu.vue"
import { MenuIcon } from '@vue-hero-icons/outline'

import { mapMutations, mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters({
      mobile: 'mobile/mobile',
    }),
  },
  components: {
    MenuIcon,
    Menu,
  },
  data() {
    return {
      isOpen: false,
    }
  },
  mounted() {
    this.isMobile()

    // Watch for window size change
    window.addEventListener("resize", this.isMobile);
  },
  unmounted() {
    window.removeEventListener("resize", this.isMobile);
  },
  methods: {
    ...mapMutations({
      isMobile: 'mobile/checkWidth',
    }),
    toggleMenu() {
      this.isOpen = !this.isOpen
    },
  },
}
</script>

<style lang="scss" scoped>
nav {
  height: 48px;
  width: 100%;
  overflow-y: hidden;
  padding: 0 8px;
  transition: height 2s;
  box-shadow: 0 2px 2px -2px;

  &.active {
    height: 300px;
    border: 2px solid $primary;
  }
 
  .navItems {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    
    .logo {

      img {
        width: 100%;
        height: 48px;
      }
    }

    .menuIcon {
      padding: 12px;
      cursor: pointer;
    }

  }

  .menu {
    width: 100%;
  }
}
</style>