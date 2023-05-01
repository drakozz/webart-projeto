<template>
  <MobileHeader @openMenu="handleMenu"></MobileHeader>
  <Header></Header>


  <MobileNavBar v-if="menuLateralIsOpen" @closeMenu="handleMenu"></MobileNavBar>
  <NavBar></NavBar>
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
  }
}
</script>


<style>
/*MEDIA RULES */
.mobileHeader {
  display: none;
}

@media screen and (max-width: 1023px) {
  .topo,
  .navBar {
    display: none
  }

  .mobileHeader {
    display: flex;
  }
}
</style>