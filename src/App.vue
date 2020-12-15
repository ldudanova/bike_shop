import Vue from 'vue'
import VueSplide from '@splidejs/vue-splide';
Vue.use( VueSplide );
<template>
  <div id="app">
    <Header/>
    <main-wrapper>

      <productCard/>

    </main-wrapper>
  <modal/>
    <Footer/>
  </div>
</template>

<script>
import mainWrapper from './components/main-wrapper'
import modal from './components/modal'
import productCard from './components/pages/product-card'

import Header from './components/elements/Header'
import Footer from "./components/elements/Footer";

export default {
  name: 'App',
  components: {
    Footer,
    Header,
    mainWrapper,
    productCard,
    modal
  }
}
</script>

<style>
#app{
  width: 100vw;
}
</style>
