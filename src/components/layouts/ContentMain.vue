<template>
  <main class="main container">
    <MobileDestaqueTopo></MobileDestaqueTopo>
    <DestaqueTopo></DestaqueTopo>
    <MobileLateralFilter @filterSelected="handleFilter"></MobileLateralFilter>

    <div class="filterProdutos">
      <div class="filterItemPage">
        <p>Itens por página: </p>
        <select name="" id="">
          <option value="">12</option>
          <option value="">24</option>
          <option value="">36</option>
        </select>
      </div>

      <div class="filterByPrice">
        <p>Ordenar por: </p>
        <select name="" id="">
          <option value="">Popularidade</option>
          <option value="">Menor Preço</option>
          <option value="">Maior Preço</option>
        </select>
      </div>
    </div>

    <div class="gridListingContainer">
      <LateralOptions @filterSelected="handleFilter"></LateralOptions>
      <ContentProdutos :filterProduto="filterProduto"></ContentProdutos>
    </div>

    <PaginationProdutos></PaginationProdutos>
  </main>
</template>
<script>

import DestaqueTopo from '../commons/DestaqueTopo.vue';
import MobileDestaqueTopo from '../mobile/MobileDestaqueTopo.vue';
import LateralOptions from '../commons/LateralOptions.vue';
import ContentProdutos from '../commons/ContentProdutos.vue';
import PaginationProdutos from '../commons/PaginationProdutos.vue';
import MobileLateralFilter from '../mobile/MobileLateralFilter.vue';

export default {
  name: 'ContentMain',
  components: {
    DestaqueTopo,
    ContentProdutos,
    LateralOptions,
    PaginationProdutos,
    MobileDestaqueTopo,
    MobileLateralFilter
  },
  data: () => ({
    filterProduto: null
  }),
  methods: {
    handleFilter(filter) {
      this.filterProduto = filter;
    }
  }
}
</script>

<style>
.gridListingContainer {
  display: grid;
  grid-template-columns: .5fr 2.5fr;
  column-gap: 40px;
}

.filterProdutos {
  display: flex;
  justify-content: flex-end;
  margin-top: 30px;
}

.filterProdutos .filterItemPage,
.filterProdutos .filterByPrice {
  display: flex;
  align-items: center;
  margin-left: 20px;
  color: var(--text-color2);
}

.filterProdutos select {
  padding: 5px;
  border-radius: 3px;
  color: var(--text-color2);
}

/*MEDIA RULES */
.mobileDestaqueTopo,
.btnFilter {
  display: none;
}


@media screen and (max-width: 1023px) {
  .destaqueTopo,
  .filterProdutos,
  aside {
    display: none;
  }

  main .mobileDestaqueTopo,
  .btnFilter{
    display: flex;
  }

  .gridListingContainer {
    display: block;
  }
}
</style>