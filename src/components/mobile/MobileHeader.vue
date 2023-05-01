<template>
  <header class="mobileHeader">
    <div class="logo">
      <font-awesome-icon icon="fa-solid fa-bars" class="icon-open" @click="openMenu" />
      <a href="#">
        <img src="@/assets/images/logo.jpg" alt="">
      </a>
    </div>

    <div class="mobileSearchBar">
      <input type="text" placeholder="Procure por produtos, marcas ou nomes...">
      <a href="#">
        <img src="@/assets/images/icons/buscar.jpg" alt="">
      </a>
    </div>
  </header>
</template>
<script>
export default {
  name: 'MobileHeader',
  methods: {
    openMenu() {
      this.$emit('openMenu', true);
    }
  }
}
</script>
<style>
.mobileHeader {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.mobileHeader .logo {
  display: flex;
  align-items: center;
}

.mobileHeader .logo svg {
  color: rgb(32, 32, 129);
  font-size: 1.7rem;
  margin-right: 20px;
}

.mobileSearchBar {
  display: flex;
  justify-content: center;
  margin-bottom: 15px;
  width: 90%;
}

.mobileSearchBar input,
.mobileSearchBar textarea {
  height: 40px;
  width: 500px;
  border: 1px solid var(--text-color2);
  border-radius: 10px 0 0 10px;
  outline: none;
}

.mobileSearchBar img {
  height: 2.6rem;
}
</style>