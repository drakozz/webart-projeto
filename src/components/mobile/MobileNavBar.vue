<template>
  <nav id="mobileNavBar">
    <div class="mobileMenuItens">
      <img src="@/assets/images/logo.jpg" alt="">

      <ul>
        <a href="">
          <li id="dropdownMenu">
            <h3>Ver toda a loja</h3>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
            <Dropdown :itens="itensMenu"></Dropdown>
          </li>
        </a>

        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-ar.jpg" alt="">
            <p>Ar Condicionado</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-eletro.jpg" alt="">
            <p>Eletrodomésticos</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-eletro2.jpg" alt="">
            <p>Eletroportatéis</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>
        

        <a href="">
          <li>
            <img src="@/assets/images/icons/industria.jpg" alt="">
            <p>Comércio e Indústria</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-pecas.jpg" alt="">
            <p>Peças</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>  


        <a href="">
          <li>
            <img src="@/assets/images/icons/icon-ferramentas.jpg" alt="">
            <p>Máquinas e Ferramentas</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
          </li>
        </a>


        <a href="">
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
export default {
  name: 'MobileNavBar'
}
</script>

<style>
  #mobileNavBar{
    margin-left: 50px;
    position: fixed;
    top: 0;
    left: -50px;
    max-height: 100vh;
    height: 100vh;
    z-index: 99999;
    background-color: #fff;
    transition: 300ms;
    overflow: hidden;
  }

  .mobileMenuItens ul li{
    display: flex;
    padding: 15px;
    color: var(--text-color);
    font-size: 1.5rem;
  }
</style>