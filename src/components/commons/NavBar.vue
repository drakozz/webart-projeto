<template>
  <nav class="navBar">
      <div class="container">
        <ul>
          <a href="">
            <li id="dropdownMenu">
              <font-awesome-icon icon="fa-solid fa-bars"/>
              <h3>Ver toda a loja</h3>
              <font-awesome-icon icon="fa-solid fa-chevron-down" />
              <Dropdown :itens="itensMenu"></Dropdown>
            </li>
          </a>

          <a href="">
            <li>
              <img src="@/assets/images/icons/icon-ar.jpg" alt="">
              <p>Ar Condicionado</p>
            </li>
          </a>

          <span class="verticalLine"></span>

          <a href="">
            <li>
              <img src="@/assets/images/icons/icon-eletro.jpg" alt="">
              <p>Eletrodomésticos</p>
            </li>
          </a>

          <span class="verticalLine"></span>

          <a href="">
            <li>
              <img src="@/assets/images/icons/icon-eletro2.jpg" alt="">
              <p>Eletroportatéis</p>
            </li>
          </a>
          
          <span class="verticalLine"></span>

          <a href="">
            <li>
              <img src="@/assets/images/icons/industria.jpg" alt="">
              <p>Comércio e Indústria</p>
            </li>
          </a>

          <span class="verticalLine"></span>

          <a href="">
            <li>
              <img src="@/assets/images/icons/icon-pecas.jpg" alt="">
              <p>Peças</p>
            </li>
          </a>  

          <span class="verticalLine"></span>

          <a href="">
            <li>
              <img src="@/assets/images/icons/icon-ferramentas.jpg" alt="">
              <p>Máquinas e Ferramentas</p>
            </li>
          </a>

          <span class="verticalLine"></span>

          <a href="">
            <li>
              <img src="@/assets/images/icons/icon-natal.jpg" alt="">
              <p>Natal</p>
            </li>
          </a>

        </ul>
      </div>
    </nav>
</template>

<script>
import Dropdown from './Dropdown.vue';

export default {
  name: 'NavBar',
  components: {
    Dropdown
  },
  data: ()=>({
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
  })
}
</script>

<style>
  /* CSS NAVBAR */

  .navBar{
    background-color: var(--bg-color);
    display: flex;
    justify-content: center;
    align-items: center;
    
  }

  .navBar ul{
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 4rem;
  }

  .navBar ul li{
    font-size: .8rem;
    padding: 0 1.5rem ;
    display: flex;
    align-items: center;
    flex-direction: column;
    color: white;
  }

  .navBar #dropdownMenu{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    background-color: white;
    height: 4rem;
    width: 15rem;
  }

  .navBar #dropdownMenu svg{
    color: rgb(32, 32, 129); 
    font-size: 1.3rem;
  }

  .navBar #dropdownMenu h3{
    color: var(--bg-color);
    font-weight: bold;
  }

  .verticalLine{
    height: 50px;
    width: 1px;
    background-color: white;
    z-index: 1;
  }
  
  #dropdownMenu:hover > .subMenu{
    display: block;
  }

</style>