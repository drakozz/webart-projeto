<template>
  <header class="container topo">
    <div class="logo">
      <a href="#">
        <img src="@/assets/images/logo.jpg" alt="">
      </a>
    </div>

    <div class="searchBar">
      <input type="text" placeholder="Procure por produtos, marcas ou nomes...">
      <a href="#">
        <img src="@/assets/images/icons/buscar.jpg" alt="">
      </a>
    </div>

    <div class="userSpace">
      <p>Olá, bem vindo(a)!</p>
      <a href="#">Entre</a>
      ou
      <a href="#">Cadastre-se</a>
    </div>

    <div class="myCart">
      <a href="#">
        <h4>Meu carrinho</h4>
      </a>
    </div>
  </header>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style >
/* CSS TOPO */
.topo {
  display: flex;
  justify-content: space-around;
  align-items: center;

}

.searchBar {
  display: flex;
  justify-content: center;
  align-items: center;
}

.searchBar input,
.searchBar textarea {
  height: 40px;
  width: 500px;
  border: 1px solid var(--text-color2);
  border-radius: 10px 0 0 10px;
  outline: none;
}

.searchBar img {
  height: 42px;
}

.searchBar a {
  margin-top: 8px;
}

.userSpace p {
  font-size: 1.1rem;
  font-weight: bold;
  color: var(--bg-color);
}

.userSpace a {
  color: black;
  font-size: .8rem;
  text-decoration: underline;
}

.myCart h4 {
  color: var(--bg-color);
  font-size: 1.1rem;
}
</style>