<template lang="">
  <section class="destaqueTopo">
    <img src="@/assets/images/destaque-topo.png" alt="">

    <div class="textoDestaque">
      <h3> Eletrodomésticos	</h3>
      <p>Você consegue imaginar sua rotina sem os eletrodomésticos? Difícil, né? Eles são equipamentos essenciais para realizar as tarefas domésticas com praticidade e eficiência, além de oferecer conforto para o seu lar. Aqui na Dufrio você encontra diversas opções de eletrodomésticos para a cozinha, a lavanderia e outros ambientes da casa. Confira as nossas dicas de compra de eletrodomésticos na Dufrio!</p>

      <a href="">Leia Mais ></a>
    </div>
        
  </section>
</template>
<script>
export default {
  name: 'DestaqueTopo'
}
</script>
<style>
  /* DESTAQUE TOPO */
.destaqueTopo{
  display: flex;
  padding: 10px;
  margin-top: 2rem;
  justify-content: space-around;
  align-items: center;
  background-color: var(--bg-color-banner);
}

.destaqueTopo .textoDestaque{
  margin-left: 5rem;
}

.destaqueTopo .textoDestaque h3{
  color: var(--bg-color);
  font-size: 1.5rem;
  margin-bottom: .5rem;
}

.destaqueTopo .textoDestaque p{
  color: var(--text-color2);
  margin-bottom: 1rem;
}

.destaqueTopo .textoDestaque a{
  color: var(--bg-color);
  padding-top: 50px;
  font-size: .8rem;
  font-weight: bold;
}
</style>