<template>
  <MobileHeader v-if="isMobile" @openMenu="handleMenu"></MobileHeader>
  <Header v-else></Header>

  <MobileNavBar v-if="isMobile" :menuLateralIsOpen="menuLateralIsOpen"></MobileNavBar>
  <NavBar v-else></NavBar>
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
    menuLateralIsOpen: null
  }),
  methods: {
    handleMenu(valor) {
      this.menuLateralIsOpen = valor;
      console.log(this.menuLateralIsOpen)
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