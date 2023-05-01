<template>
  <div>
    <Topo></Topo>
    
    <ContentMain>
    </ContentMain>
    
    <Footer></Footer>
  </div>
</template>

<script>
import Topo from './components/layouts/Topo.vue';
import ContentMain from './components/layouts/ContentMain.vue';
import Footer from './components/layouts/Footer.vue';


export default {
  name:'App',
  components: {
    Topo,
    ContentMain,
    Footer
  }

}
</script>

<style>

:root
{
  --text-color: black;
  --text-color2: rgb(126, 126, 126);
  --text-color3: rgb(44, 138, 226);
  --bg-color: #ff4f01;
  --bg-color-banner: #edf5f8;
  --color-button-buy: #06cc84;
  --color-button-hover: #038354;


  --title-font: "Montserrat", sans-serif;
  --text-font2: "Poppins", sans-serif;
  --text-font: "Work Sans", sans-serif;
}

*
{
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
}

a {
    text-decoration: none;
    font-size: 18px;
}

.container{
  max-width: 1120px;
  margin: 0 auto;
}

/* ROUTES */
.routes{
  display: flex;
  margin-top: 20px;
}

.routes p{
  font-size: .8rem;
  color: var(--text-color2);
}

.routes span{
  color: var(--bg-color);
  font-weight: bold;
}


</style>
