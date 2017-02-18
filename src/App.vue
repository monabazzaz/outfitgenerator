<template>
  <div id="app">
    <hello></hello>
    <selected :top="currentTop" :bottom="currentBottom" :shoe="currentShoe"></selected>
    <tops @selected="onSelectedTop"></tops>
    <bottoms @selected="onSelectedBottom"></bottoms>
    <shoes @selected="onSelectedShoe"></shoes>
    <footer></footer>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Selected from './components/Selected'
import Tops from './components/Tops'
import Bottoms from './components/Bottoms'
import Shoes from './components/Shoes'
import Footer from './components/Footer'

export default {
  name: 'app',
  components: {
    Hello,
    Selected,
    Tops,
    Bottoms,
    Shoes,
    Footer
  },
  data () {
    return {
      currentTop: null,
      currentBottom: null,
      currentShoe: null
    }
  },
  methods: {
    onSelectedTop (top) {
      console.log('App -> onSelectedTop')
      this.currentTop = top
    },
    onSelectedBottom (bottom) {
      console.log('App -> onSelectedBottom')
      this.currentBottom = bottom
    },
    onSelectedShoe (shoe) {
      console.log('App -> onSelectedShoe')
      this.currentShoe = shoe
    }
  }
}
</script>

<style>
#app {
  text-align: center;
}
body {
    background: url(/static/images/birds.png);
    background-repeat: repeat;
    background-attachment: fixed;
    background-position: center;
    background-size: cover;
    }

@media screen and (max-width: 1100px) {

#app {
  text-align: center;
}

body {
  text-align: center;
}
}
</style>
