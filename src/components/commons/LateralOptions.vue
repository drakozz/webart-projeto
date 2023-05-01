<template>
  <aside class="lateralOptions">
    <div class="category">
      <h3>Categorias</h3>
      <ul>
        <li>
          <a href="#">Adega de Vinho</a>
        </li>
        <li>
          <a href="#">Churrasqueira Elétrica</a>
        </li>
        <li>
          <a href="#">
            Churrasqueira
          </a>
        </li>
        <li>
          <a href="#">
            Coifa
          </a>
        </li>
        <li>
          <a href="#">
            Cooktop
          </a>
        </li>
        <li>
          <a href="#">
            Depurador de Ar
          </a>
        </li>
        <li>
          <a href="#">
            Fogão a Gás
          </a>
        </li>
        <li>
          <a href="#">Forno a Gás</a>
        </li>
        <li>
          <a href="#">Forno Elétrico</a>
        </li>
        <li>
          <a href="#">Frigobar</a>
        </li>
        <span>
          <a href="#">Ver Mais</a>
        </span>
      </ul>
    </div>

    <h3>Marcas</h3>

    <div class="prices">
      <h3>Preço</h3>

      <div class="priceOptions">
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
      </div>
    </div>
  </aside>
</template>

<script>

export default {
  name: 'LateralOptions',
  data: () => ({
    filterPrice: null
  }),
  methods: {
    filterProdutos() {
      this.$emit('filterSelected', this.filterPrice)
    }
  }
}

</script>

<style>
.lateralOptions {
  margin-top: 50px;
}

.lateralOptions h3 {
  color: var(--bg-color);
  font-size: 1rem;
  margin-bottom: 10px;
}

.lateralOptions .category {
  margin-bottom: 30px;
}

.lateralOptions .category ul li a,
.lateralOptions .category span a {
  color: var(--text-color2);
  font-size: .8rem;
}

.lateralOptions .category span {
  text-decoration: underline;
}

.lateralOptions .priceOptions fieldset {
  margin-bottom: 5px;
  border: none;
}

.prices .priceOptions {
  font-size: .8rem;
  color: var(--text-color2);
}
</style>