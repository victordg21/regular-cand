<script>
import Header from './components/Header.vue'
import Banner from './components/Banner.vue'
import About from './components/About.vue'
import Informations from './components/Informations.vue'
import Article from './components/Article.vue'
import Date from './components/Date.vue'
import Maps from './components/Maps.vue'
import Faq from './components/Faq.vue'
import Contact from './components/Contact.vue'


export default {
  
  components:{
    Header,
    Banner,
    About,
    Informations,
    Date,
    Article,
    Maps,
    Faq,
    Contact
  },
};
</script>

<template>
  <Header id="Início"/>
  <div class="sticky">
    <Banner/>
    <About id="Sobre Nós"/>
    <Informations/>
    <Date/>
    <Article id="Artigos"/>
    <Maps id="Localização"/>
    <Faq/>
    <Contact id="Contato"/>
    <footer>
      <h2 class="text-center py-2">© Desenvolvido por João Victor Dias Gonçalves - 2024</h2>
    </footer>
  </div>
</template>

<style scoped>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  overflow-x: hidden;
}

.container{
  max-width: 1280px;
  width: 100%;
  margin: 0 auto;
}



</style>

