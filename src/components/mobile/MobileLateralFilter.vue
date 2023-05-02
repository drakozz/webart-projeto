<template>
  <div class="btnFilter" @click="openFilter">
    <a href="#">Filtrar</a>
  </div>
  <div class="mobileLateralFilter" v-if="filterIsOpen">

    <div class="lateralFilter">
      <font-awesome-icon icon="fa-solid fa-xmark" class="icon-close" @click.prevent="openFilter" />
      <div class="category">
        <h3>Categorias</h3>
        <select name="" id="" @change="selectCategory">
          <option value="">Todos</option>
          <option value="1">Adega de Vinho</option>
          <option value="2">Churrasqueira Elétrica</option>
          <option value="3">Churrasqueira</option>
          <option value="4">Coifa</option>
          <option value="5">Micro-ondas</option>
          <option value="6">Cooktop</option>
          <option value="7">Depurador de Ar</option>
          <option value="8">Fogão a Gás</option>
          <option value="9">Forno a Gás</option>
          <option value="10">Forno Elétrico</option>
          <option value="11">Frigobar</option>
          <option value="12">Geladeira</option>
          <option value="13">Lava e Seca</option>
        </select>
      </div>

      <div class="priceOptions">
        <h3>Preço</h3>
        <fieldset>
          <input type="radio" id="priceOptions1" name="priceOptions" value="665.00-5575.00" v-model="filterPrice"
            @change="filterProdutos">
          <label for="priceOptions1"> R$665,00 a 5573,00</label><br>
        </fieldset>

        <fieldset>
          <input type="radio" id="priceOptions2" name="priceOptions" value="5573.01-10480.00" v-model="filterPrice"
            @change="filterProdutos">
          <label for="priceOptions2"> R$5573,01 - 10480,00</label><br>
        </fieldset>

        <fieldset>
          <input type="radio" id="priceOptions3" name="priceOptions" value="10480.01-15388.00" v-model="filterPrice"
            @change="filterProdutos">
          <label for="priceOptions3"> R$10480,01 - 15388,00</label><br>
        </fieldset>

        <fieldset>
          <input type="radio" id="priceOptions4" name="priceOptions" value="15388.01-20295.00" v-model="filterPrice"
            @change="filterProdutos">
          <label for="priceOptions4"> R$15388,01 - 20295,00</label><br>
        </fieldset>

        <fieldset>
          <input type="radio" id="priceOptions5" name="priceOptions" value="20295.01-25203.00" v-model="filterPrice"
            @change="filterProdutos">
          <label for="priceOptions5"> R$20295,01 - 25203,00</label>
        </fieldset>

        <fieldset>
          <input type="radio" id="limparFiltro" name="priceOptions" value="0.00-25203.00" v-model="filterPrice"
            @change="filterProdutos">
          <label for="limparFiltro"> Limpar filtro</label>
        </fieldset>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'MobileLateralFilter',
  data: () => ({
    filterPrice: null,
    filterCategory: null,
    filterIsOpen: false
  }),
  methods: {
    filterProdutos() {
      this.$emit('filterSelected', this.filterPrice)
      this.filterIsOpen = !this.filterIsOpen
    },
    openFilter() {
      return this.filterIsOpen = !this.filterIsOpen
    },
    selectCategory(e) {
      this.filterCategory = e.target.value
      this.$emit('categorySelected', this.filterCategory)
    }
  },
  emits: ["filterSelected", "categorySelected"]

}
</script>
<style scoped>
.btnFilter {
  max-width: 100vw;
  padding: 30px;
}

.btnFilter a {
  display: block;
  text-align: center;
  padding: 15px 0;
  border-radius: 5px;
  background-color: var(--bg-color);
  color: white;
  font-size: .8rem;
  font-weight: bold;
  width: 100%;
}

.icon-close {
  position: absolute;
  top: 20px;
  right: 70px;
  font-size: 2.5rem;
  color: var(--bg-color);
}

.mobileLateralFilter {
  position: fixed;
  top: 0;
  right: -50px;
  max-width: 80vw;
  max-height: 100vh;
  width: 90vw;
  height: 100vh;
  z-index: 99999;
  background-color: #fff;
  overflow: hidden;
}


.mobileLateralFilter .lateralFilter {
  padding: 30px;
  font-size: .8rem;
  color: var(--text-color2);
}

.lateralFilter h3 {
  font-size: 1rem;
  color: var(--bg-color);
  margin-bottom: 10px;
}

.lateralFilter fieldset {
  display: flex;
  align-items: center;
  margin-bottom: 5px;
  border: none;
}

.category {
  margin-top: 50px;
}

.category select {
  margin-bottom: 20px;
}
</style>