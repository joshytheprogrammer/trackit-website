<template>
  <nav :class="{ active: isOpen }">
    <div class="navItems">
      <div class="logo">
        <Nuxt-Link to="/"><img src="../../assets/img/logo.jpg" alt="Track I.T. Logo"></Nuxt-Link>
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
  height: 90px;
  width: 100%;
  overflow-y: hidden;
  padding: 14px 8px;
  transition: height 2s;
  box-shadow: 0 2px 2px -2px;
  background: $light;

  &.active {
    height: 300px;
  }
 
  .navItems {
    display: flex;
    justify-content: space-between;
    align-items: center;
    
    .logo {
      width: 72px;
      
      img {
        width: 100%;
        height: 70px;
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