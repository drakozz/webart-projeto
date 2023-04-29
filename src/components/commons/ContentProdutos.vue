<template>
    <section class="contentProdutos">

        <div class="cardProdutos" v-for="(produto, i) in dataProdutos" :key="i">
          <img :src="require(`@/assets/images/produtos/${produto.imagem}`) " alt="">

          <h3 class="descontoProduto">{{produto.desconto}}</h3>
          <p>{{produto.nome}}</p>

          <div class="selos">
            <div class="seloFrete">
              <img v-if="produto.selos.freteGratis !== '' " :src="require(`@/assets/images/selos/${produto.selos.freteGratis}`)" alt="">
            </div>

            <div class="seloMarca">
              <img :src="require(`@/assets/images/selos/${produto.selos.marca}`)" alt="">
            </div>

            <img v-if="produto.selos.voltagem !== '' " :src="require(`@/assets/images/selos/${produto.selos.voltagem}`)" alt="" >
            <img v-if="produto.selos.procel !== '' " :src="require(`@/assets/images/selos/${produto.selos.procel}`)" alt="" >
          </div>

          <h2>R$ {{produto.preco}}</h2>
          <small>
            <span>à vista no PIX ou boleto</span>
            <br>
            ou R$ 1665,70 em 10x de R$166,57 sem juros
          </small>
          
          <button class="buttonAddCart">
            <font-awesome-icon icon="fa-solid fa-cart-shopping" />
            Adicionar ao carrinho
          </button>
        </div>
    </section>
</template>

<script>
import ProdutosData from '@/data/ProdutosData.json'

export default {
    name: 'ContentProdutos',
    data: () => ({
    dataProdutos: ProdutosData
  })
}
</script>

<style>
    /*CSS CARD PRODUTOS*/
  .contentProdutos{
    margin-top: 50px;
    display: flex;
    flex-wrap: wrap;
  }

  .cardProdutos{
    position: relative;
    display: flex;
    justify-content: center;
    flex-direction: column;
    width: 300px;
    text-align: center;
    padding: 30px;
  }

  .cardProdutos:hover{
    border: 1px solid var(--text-color2);
  }

  .cardProdutos .descontoProduto{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: black;
    color: white;
    width: 70px;
    height: 25px;
    border-radius: 3px;
    font-size: .8rem;
    margin-bottom: 10px;
  }

  .cardProdutos .selos{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 10px;
  }

  .cardProdutos .selos .seloMarca{
    margin-top: 30px;
    flex: 1 1 100%; 
  }

  .cardProdutos .selos .seloFrete{
    position: absolute;
    left: 10px;
    top: 10px;
  }

  .cardProdutos .selos .seloMarca img{
    width: 150px;
  }

  .cardProdutos h2, 
  .cardProdutos span{
    color: var(--text-color3);
    font-weight: bold;
  }

  .cardProdutos .buttonAddCart{
    font-size: 1rem;
    font-weight: bold;
    border: none;
    background-color: var(--color-button-buy);
    color: white;
    height: 50px;
    border-radius: 5px;
    margin-top: 10px;
    transition: .5s;
  }

  .cardProdutos .buttonAddCart:hover{
    background-color: var(--color-button-hover);
    cursor: pointer;
  }

</style>