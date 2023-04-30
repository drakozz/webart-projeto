<template>
  <section class="mobileDestaqueTopo">

    <div class="destaque">
      <img src="@/assets/images/destaque-topo.png" alt="">

      <div class="textoDestaque">
        <h3> Eletrodomésticos </h3>
        <p>Você consegue imaginar sua rotina sem os eletrodomésticos? Difícil, né? Eles são equipamentos essenciais para
          realizar as tarefas domésticas com praticidade e eficiência, além de oferecer conforto para o seu lar. Aqui na
          Dufrio você encontra diversas opções de eletrodomésticos para a cozinha, a lavanderia e outros ambientes da
          casa. Confira as nossas dicas de compra de eletrodomésticos na Dufrio!</p>

        <a href="#" @click.prevent="destaqueMostrarMais = !destaqueMostrarMais">Leia Mais ></a>
      </div>
    </div>

    <div class="mostrarMais" v-show="destaqueMostrarMais">
      <h3>Tipos de eletrodoméstico</h3>
      <p>
        Quando o assunto é eletrodoméstico, o que não falta é a variedade de equipamentos para facilitar sua vida em
        diversos aspectos.

        São aparelhos que te ajudam no dia a dia a cozinhar, lavar louça, lavar roupas, secar, conservar, esquentar e
        refrigerar alimentos, entre muitas outras funções. Veja só:
      </p>

      <h3>Cozinha</h3>
      <p>
        A cozinha é, provavelmente, a peça da casa que concentra o maior número de eletrodomésticos.

        Os equipamentos centrais do ambiente são os refrigeradores, responsáveis por armazenar e conservar alimentos
        não-perecíveis; e os fogões, que podem ter dois tipos de funcionamento: fogão a gás e fogão elétrico.
        Em alternativa ao fogão tradicional, existe o cooktop, equipamento que não traz forno a gás embutido, apenas o
        tampo com as bocas e o painel de acendimento. Já para aqueles que têm pouco espaço na cozinha, os frigobares são
        ótimos.
        Não podemos esquecer, é claro, da coifa e do depurador, equipamentos instalados acima do fogão, super úteis para
        dissipar a fumaça e a gordura da comida.
        Além dos eletrodomésticos tradicionais, uma cozinha funcional não pode deixar de contar com outros aparelhos que
        facilitam a rotina, como o microondas. Afinal, não tem jeito mais rápido e fácil de aquecer a comida!
        Ainda no campo do preparo dos alimentos, outro equipamento imprescindível na cozinha é o forno elétrico, uma opção
        compacta e prática para assados.
        E para quem tem a rotina corrida e não abra mão da praticidade, a máquina lava-louça é mais uma grande aliada no
        dia a dia.
      </p>

      <h3>Lavanderia</h3>
      <p>
        A lavanderia é outra área da casa onde você pode se beneficiar (e muito) da ajuda dos eletrodomésticos.

        O tanquinho é um aparelho super prático para lavar a roupa. Conta com funções simples e tamanho mais enxuto,
        perfeito para quem tem pouco espaço na lavanderia.
        Agora, para quem tem uma área maior e precisa de funções mais avançadas e automatizadas, como diferentes programas
        de lavagem, o ideal é ter uma boa máquina de lavar.
        A centrífuga de roupas é ótima para quem não tem máquina de lavar, já que ela executa a função de centrifugar,
        retirando o excesso de água das peças. Agiliza bastante o tempo de secagem no varal.
        Já nas regiões de inverno frio e úmido, em que as roupas custam a secar, ajuda muito ter uma secadora de roupas. É
        só colocar as peças no equipamento e programar a secagem que elas saem prontinhas para guardar.
        A lava-seca está entre as melhores opções de equipamentos para cuidados com as roupas, porque é uma máquina 2 em
        1. Ela agrega as funções de lavagem e secagem, otimizando espaço na lavandeira e proporcionando ainda mais
        praticidade.
      </p>


      <h3>Sala e espaços de lazer</h3>
      <p>Nem só de tarefas domésticas é feito seu tempo em casa, certo? Alguns eletrodomésticos também podem proporcionar
        momentos incríveis de diversão e prazer.
        A TV LED gera imagens de alta qualidade, com nitidez e contraste superiores a outros modelos do mercado. Além
        disso, é mais econômica. Perfeita para assistir a seus filmes e séries preferidos!
        Cheia de funcionalidades, a TV Smart proporciona uma incrível experiência em termos de conectividade. Com ela,
        você pode assistir Netflix, Spotify, Youtube e todas as suas plataformas preferidas da internet. Isso sem falar da
        alta qualidade de som e imagem.
        Nada melhor do que assistir à TV apreciando uma boa cerveja, não é? A cervejeira residencial tem espaço interno
        otimizado e refrigeração especial, ajudando a conservar suas bebidas da melhor maneira possível.
        Já para quem prefere outros tipos de bebida, a adega para vinhos e a champanheira podem ser os equipamentos
        ideais.
      </p>

      <h3>Dicas para escolher eletrodoméstico</h3>
      <p>A escolha de um eletrodoméstico para sua casa deve levar em conta diversos fatores. Lembrando que vários desses
        equipamentos têm alto valor de investimento e longa duração, então é importante ter cuidado para fazer a compra
        certa.</p>

      <h3>Tamanho</h3>
      <p>Independente do tipo de eletrodoméstico que você for comprar, considere seu tamanho e também as dimensões do
        cômodo onde pretende instalá-lo. Esse cuidado é especialmente importante na cozinha, onde vários aparelhos
        precisam dividir um espaço restrito.</p>

      <h3>Voltagem</h3>
      <p>Antes de ir à loja, verifique a tensão elétrica da sua casa e certifique-se de que o eletrodoméstico escolhido
        tem a voltagem correta. Uma compra errada pode resultar em equipamentos queimados ou toda aquela função para fazer
        a troca.</p>

      <h3>Selo Procel</h3>
      <p>O Selo Procel atesta a eficiência energética dos equipamentos elétricos. Se a economia de energia é um critério
        importante para você na escolha dos eletrodomésticos, fique atento a esse detalhe.</p>

      <h3>Estética</h3>
      <p>A estética dos equipamentos faz toda a diferença no visual da sua casa. Os eletrodomésticos coloridos estão em
        alta, compondo uma decoração moderna e divertida. É importante observar também o design e o material de
        fabricação.</p>

      <span @click.prevent="destaqueMostrarMais = !destaqueMostrarMais">Recolher</span>
    </div>

  </section>
</template>
<script>
export default {
  name: 'MobileDestaqueTopo',
  data: ()=>({
    destaqueMostrarMais: false
  })
}
</script>
<style>
/* DESTAQUE TOPO */
.destaque {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.destaque img{
  width: 90%;
}

.mobileDestaqueTopo {
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding: 10px;
  margin-top: 2rem;
  background-color: var(--bg-color-banner);
}

.mobileDestaqueTopo .textoDestaque {
  max-width: 100vw;
  padding: 20px;
}

.mobileDestaqueTopo .textoDestaque h3,
.mobileDestaqueTopo .mostrarMais h3 {
  color: var(--bg-color);
  font-size: 1.5rem;
  margin-bottom: .5rem;
  text-align: center;
}

.mobileDestaqueTopo .textoDestaque p,
.mobileDestaqueTopo .mostrarMais p {
  color: var(--text-color2);
  margin-bottom: 1rem;
}

.mobileDestaqueTopo .textoDestaque a,
.mobileDestaqueTopo .mostrarMais span {
  color: white;
  width: 100%;
  display: block;
  text-align: center;
  padding: 15px 0;
  border-radius: 5px;
  background-color: var(--bg-color);
  font-size: .8rem;
  font-weight: bold;
}

.mobileDestaqueTopo .mostrarMais {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 30px;
}


</style>