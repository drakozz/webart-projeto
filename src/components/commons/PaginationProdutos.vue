<template>
  <div class="paginationProdutos">
        <div></div>
        <div class="pagination">
          <span>Produtos: 1-12 de 284 encontrado(s)</span>
          <a href="#" class="" title=""> Primeira</a>
          <a href="#"> Anterior</a>

          <button class="paginationButton selected" >
            1
          </button>

          <button class="paginationButton" v-for="(number, i) in 4" :key="i">
            {{ number+1 }}
          </button>

          <a href="#" class="" title="">Próximo </a>
          <a href="#">Última</a>
        </div>
      </div>
</template>
<script>
export default {
  name: 'PaginationProdutos'
}
</script>
<style>
  .paginationProdutos{
  display: grid;
  grid-template-columns: .5fr 2.5fr;
  margin-top: 50px;
  width: 100%;
  }

  .paginationProdutos span,
  .paginationProdutos a{
  color: var(--text-color2);
  font-size: 1rem;
  margin: 0 20px;
  }

  .paginationProdutos .paginationButton{
  padding: 10px 15px;
  background-color: white;
  color: var(--text-color2);
  border: none;
  border-radius: 3px;
  }

  .paginationProdutos .selected{
  color: white;
  background-color: var(--bg-color);
  }

  .paginationProdutos .selected:hover,
  .paginationProdutos .paginationButton:hover{
  cursor: pointer;
  }
</style>