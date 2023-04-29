<template>
  <main class="main container">
      <DestaqueTopo></DestaqueTopo>

      <div class="gridListingContainer">
        <LateralOptions></LateralOptions>
        <ContentProdutos></ContentProdutos>
      </div>
          
  </main>
</template>
<script>

import DestaqueTopo from '../commons/DestaqueTopo.vue';
import LateralOptions from'../commons/LateralOptions.vue';
import ContentProdutos from '../commons/ContentProdutos.vue';

export default {
  name: 'ContentMain',
  components: {
    DestaqueTopo,
    ContentProdutos,
    LateralOptions
  }
}
</script>

<style>

.gridListingContainer{
  display: grid;
  grid-template-columns: .5fr 2.5fr;
  column-gap: 40px;
}



</style>