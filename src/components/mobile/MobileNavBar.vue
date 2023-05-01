<template>
  <font-awesome-icon icon="fa-solid fa-xmark" class="icon-close" v-if="menu" @click.prevent="closeMenu"/>
  <nav id="mobileNavBar" v-show="menu">
    <div class="logo">
      <img src="@/assets/images/logo.jpg" alt="">
    </div>

    <div class="mobileMenuItens">
      <ul>
        <a href="">
          <li id="dropdownMenuMobile">
            <h3>Ver toda a loja</h3>
            <font-awesome-icon icon="fa-solid fa-chevron-right"/>
            <Dropdown :itens="itensMenu"></Dropdown>
          </li>
        </a>

        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-ar.jpg" alt="">
            <p>Ar Condicionado</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right"/>
          </li>
        </a>


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-eletro.jpg" alt="">
            <p>Eletrodomésticos</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right"/>
          </li>
        </a>


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-eletro2.jpg" alt="">
            <p>Eletroportatéis</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right"/>
          </li>
        </a>
        

        <a href="">
          <li>
            <img src="@/assets/images/icons/industria.jpg" alt="">
            <p>Comércio e Indústria</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right"/>
          </li>
        </a>


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-pecas.jpg" alt="">
            <p>Peças</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right"/>
          </li>
        </a>  


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-ferramentas.jpg" alt="">
            <p>Máquinas e Ferramentas</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right"/>
          </li>
        </a>


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-natal.jpg" alt="">
            <p>Natal</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right"/>
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
    menuIsOpen: true,
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
  components:{
    Dropdown
  },
  props: {
    menuLateralIsOpen: {
      type: Boolean,
      default: false
    }
  },
  computed:{
    menu(){
      return this.menuIsOpen && this.menuLateralIsOpen
    }
  },
  methods: {
    closeMenu(){
      this.menuIsOpen = false
      console.log('ta chamando', this.menuIsOpen, this.menu)
    }
  }
}
</script>

<style>
  .icon-close{
    position: absolute;
    top: 20px;
    right: 20px;
    font-size: 3.5rem;
    color: var(--bg-color);
  }

  #mobileNavBar{
    margin-left: 50px;
    position: fixed;
    top: 0;
    left: -50px;
    max-width: 80vw;
    max-height: 100vh;
    height: 100vh;
    z-index: 99999;
    background-color: #fff;
    transition: 300ms;
    overflow: hidden;
  }

  #mobileNavBar .logo{
    display: flex;
    justify-content: center;
    margin: 60px 0 60px 0;
  }

  #mobileNavBar .logo img{
    width: 60%;
  }
  

  .mobileMenuItens #dropdownMenuMobile{
    color: var(--bg-color);
    font-size: 1rem;
  }

  .mobileMenuItens ul li{
    display: flex;
    align-items: center;
    padding: 15px;
    color: var(--text-color2);
    font-size: 1rem;
  }

  .mobileMenuItens ul li img{
    width: 20px;
    margin-right: 50px;
  }
</style>