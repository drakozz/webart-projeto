<template >
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
</style>