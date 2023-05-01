<template>
  <nav id="mobileNavBar">
    <font-awesome-icon icon="fa-solid fa-xmark" class="icon-close" @click.prevent="closeMenu" />
    <div class="logo">
      <img src="@/assets/images/logo.jpg" alt="">
    </div>

    <div class="mobileMenuItens">
      <ul>
        <a href="#">
          <li id="dropdownMenuMobile">
            <h3>
              Ver toda a loja
              <font-awesome-icon icon="fa-solid fa-chevron-right" />
            </h3>
            <Dropdown :itens="itensMenu"></Dropdown>
          </li>
        </a>

        <a href="#">
          <li>
            <img src="@/assets/images/icons/icon-ar.jpg" alt="">
            <p>Ar Condicionado</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="#">
          <li>
            <img src="@/assets/images/icons/icon-eletro.jpg" alt="">
            <p>Eletrodomésticos</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="#">
          <li>
            <img src="@/assets/images/icons/icon-eletro2.jpg" alt="">
            <p>Eletroportatéis</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="#">
          <li>
            <img src="@/assets/images/icons/industria.jpg" alt="">
            <p>Comércio e Indústria</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="#">
          <li>
            <img src="@/assets/images/icons/icon-pecas.jpg" alt="">
            <p>Peças</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="#">
          <li>
            <img src="@/assets/images/icons/icon-ferramentas.jpg" alt="">
            <p>Máquinas e Ferramentas</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="#">
          <li>
            <img src="@/assets/images/icons/icon-natal.jpg" alt="">
            <p>Natal</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>

      </ul>
    </div>
  </nav>
</template>

<script>
import Dropdown from '../commons/Dropdown.vue';

export default {
  name: 'MobileNavBar',
  data: () => ({
    itensMenu: [
      {
        title: 'Ar Condicionado',
        link: '#'
      },
      {
        title: 'Ventilação',
        link: '#'
      },
      {
        title: 'Eletrodomésticos',
        link: '#'
      },
      {
        title: 'Eletroportáteis',
        link: '#'
      },
      {
        title: 'Casa Inteligente',
        link: '#'
      },
      {
        title: 'Comércio e Indústria',
        link: '#'
      },
      {
        title: 'Máquinas e Ferramentas',
        link: '#'
      },
      {
        title: 'Materiais de Instalação',
        link: '#'
      },
      {
        title: 'Fluído Gás Refrigerante',
        link: '#'
      },
      {
        title: 'Peças',
        link: '#'
      }
    ]
  }),
  components: {
    Dropdown
  },
  methods: {
    closeMenu() {
      this.$emit('closeMenu', false);
    }
  }
}
</script>

<style scoped>
.icon-close {
  position: absolute;
  top: 20px;
  right: 20px;
  font-size: 2.5rem;
  color: var(--bg-color);
}

#mobileNavBar {
  margin-left: 50px;
  position: fixed;
  top: 0;
  left: -50px;
  max-width: 80vw;
  max-height: 100vh;
  width: 90vw;
  height: 100vh;
  z-index: 99999;
  background-color: #fff;
  transition: 300ms;
  overflow: hidden;
}

#mobileNavBar .logo {
  display: flex;
  justify-content: center;
  margin: 60px 0 60px 0;
}

#mobileNavBar .logo img {
  width: 60%;
}


.mobileMenuItens #dropdownMenuMobile {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  color: var(--bg-color);
  font-size: 1rem;
}

.mobileMenuItens #dropdownMenuMobile h3{
  display: flex;
  width: 100%;
  justify-content: space-between;
}

.mobileMenuItens #dropdownMenuMobile .subMenu{
  display: none;
}

.mobileMenuItens ul li {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px;
  color: var(--text-color2);
  font-size: 1rem;
}

.mobileMenuItens ul li img {
  width: 20px;
  margin-right: 10px;
}

</style>