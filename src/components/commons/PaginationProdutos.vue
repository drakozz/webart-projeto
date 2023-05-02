<template>
  <div class="paginationProdutos">
    <div></div>
    <div class="pagination">
      <span>Produtos: 1-12 de 284 encontrado(s)</span>
      <font-awesome-icon icon="fa-solid fa-chevron-left" />
      <font-awesome-icon icon="fa-solid fa-chevron-left" />
      <a href="#" class="" title=""> Primeira</a>

      <font-awesome-icon icon="fa-solid fa-chevron-left" />
      <a href="#"> Anterior</a>

      <button class="paginationButton selected">
        1
      </button>

      <button class="paginationButton" v-for="(number, i) in 4" :key="i">
        {{ number + 1 }}
      </button>

      <a href="#" class="" title="">Próximo </a>
      <font-awesome-icon icon="fa-solid fa-chevron-right" />

      <a href="#">Última</a>
      <font-awesome-icon icon="fa-solid fa-chevron-right" />
      <font-awesome-icon icon="fa-solid fa-chevron-right" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'PaginationProdutos'
}
</script>
<style>
/* PAGINAÇÃO DE PRODUTOS */
.pagination {
  display: flex;
  justify-content: center;
  align-items: center;
}

.pagination svg {
  color: rgb(133, 133, 133);
  font-size: .8rem;
}

.paginationProdutos {
  display: grid;
  grid-template-columns: .5fr 2.5fr;
  margin-top: 50px;
  width: 100%;
}

.paginationProdutos span,
.paginationProdutos a {
  color: var(--text-color2);
  font-size: 1rem;
  margin: 0 20px;
}

.paginationProdutos .paginationButton {
  padding: 10px 15px;
  background-color: white;
  color: var(--text-color2);
  border: none;
  border-radius: 3px;
}

.paginationProdutos .selected {
  color: white;
  background-color: var(--bg-color);
}

.paginationProdutos .selected:hover,
.paginationProdutos .paginationButton:hover {
  cursor: pointer;
}

/* ALTERAÇOES MOBILE */
@media screen and (max-width: 1023px) {
  .paginationProdutos {
    display: flex;
  }

  .pagination {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
  }

  .pagination span {
    width: 100%;
    text-align: center;
    margin-bottom: 20px;
  }

  .pagination a,
  .pagination svg {
    display: none;
    visibility: hidden;
  }
}
</style>