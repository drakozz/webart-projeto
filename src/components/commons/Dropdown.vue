<template>
  <div class="subMenu">
    <ul>
      <li v-for="(item, i) in itens" :key="i">
        <a :href="item.link">{{ item.title }}</a>
        <font-awesome-icon icon="fa-solid fa-chevron-right" style="color: rgb(133, 133, 133); font-size: 1rem" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Dropdown',
  props: ['title', 'itens'],

}
</script>

<style>
/* DROPDOWN */
#dropdownMenu {
  position: relative;
}

.navBar .subMenu {
  display: none;
  position: absolute;
  z-index: 1;
  top: 60px;
  left: 0;
}

.navBar .subMenu ul {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  background-color: white;
  width: 240px;
}

.navBar .subMenu li {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 100%;
  background-color: white;
}

.navBar .subMenu li a {
  font-size: .8rem;
  color: black;
  padding: 1rem 0;
}

/* ALTERAÇOES MOBILE */
@media screen and (max-width: 1023px) {
  #dropdownMenuMobile .subMenu ul li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 0;

  }

  #dropdownMenuMobile .subMenu ul li a {
    color: var(--text-color2);
    font-size: .8rem;
  }
}
</style>