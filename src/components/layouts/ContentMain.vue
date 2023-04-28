<template lang="">
  <main class="main container">
      <DestaqueTopo></DestaqueTopo>

      <section class="Produtos">

        <div class="listagemProdutos"></div>

        <div class="cardProdutos">
          
        </div>
      </section>
  </main>
</template>
<script>

import DestaqueTopo from '../commons/DestaqueTopo.vue';
import ProdutosData from '@/data/ProdutosData.json'

export default {
  name: 'ContentMain',
  components: {
    DestaqueTopo,
  },

  data: () => ({
    dataProdutos: ProdutosData
  })
}
</script>
<style lang="">
  
</style>