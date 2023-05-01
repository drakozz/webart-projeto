<template>
  <MobileHeader v-if="isMobile" @openMenu="handleMenu"></MobileHeader>
  <Header v-else></Header>


  <MobileNavBar v-if="isMobile && menuLateralIsOpen" @closeMenu="handleMenu"></MobileNavBar>
  <NavBar v-else-if="!isMobile"></NavBar>
</template>

<script>
import Header from '../commons/Header.vue';
import NavBar from '../commons/NavBar.vue';
import MobileHeader from '../mobile/MobileHeader.vue'
import MobileNavBar from '../mobile/MobileNavBar.vue';

export default {
  components: {
    Header,
    NavBar,
    MobileHeader,
    MobileNavBar
  },
  data: () => ({
    menuLateralIsOpen: false
  }),
  methods: {
    handleMenu(valor) {
      this.menuLateralIsOpen = valor;
    }
  },
  computed: {
    isMobile() {
      return window.innerWidth < 768;
    }
  }
}
</script>


<style></style>