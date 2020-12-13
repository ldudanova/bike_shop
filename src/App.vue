import Vue from 'vue'
<template>
  <div id="app">
    <Header/>
    <main-wrapper>
      <productCard/>

    </main-wrapper>

  </div>
</template>

<script>
import mainWrapper from './components/main-wrapper'
import productCard from './components/pages/product-card'

import Header from './components/elements/Header'

export default {
  name: 'App',
  components: {
    mainWrapper,
    Header,
    productCard
  }
}
</script>

<style>

</style>
