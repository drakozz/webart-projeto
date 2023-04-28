<template lang="">
  <main class="main container">
      <DestaqueTopo></DestaqueTopo>

      <section class="listagemProdutos">
        <div class="cardProdutos" v-for="(produto, i) in dataProdutos" :key="i">
          <p>{{produto.nome}}</p>
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