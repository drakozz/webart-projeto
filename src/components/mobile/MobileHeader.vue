<template>
  <header class="mobileHeader">
    <div class="logo">
      <font-awesome-icon icon="fa-solid fa-bars"/>
      <a href="">
        <img src="@/assets/images/logo.jpg" alt="">
      </a>
    </div>

    <div class="mobileSearchBar">
      <input type="text" placeholder="Procure por produtos, marcas ou nomes...">
      <a href="">
        <img src="@/assets/images/icons/buscar.jpg" alt="">
      </a>
    </div>
  </header>
</template>
<script>
export default {
  name: 'MobileHeader'
}
</script>
<style>
  .mobileHeader{
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .mobileHeader .logo{
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .mobileHeader .logo svg{
    color: rgb(32, 32, 129); 
    font-size: 1.7rem;
    margin-right: 20px;
  }

  .mobileSearchBar{
    display: flex;
    justify-content: center;
    margin-bottom: 15px;
    width: 80%;
  }

  .mobileSearchBar input, 
  .mobileSearchBar textarea{
  height: 50px;
  width: 500px;
  border: 1px solid var(--text-color2);
  border-radius: 10px 0 0 10px;
  outline: none;
  }

  .mobileSearchBar img{
    height: 3.2rem;
  }
</style>