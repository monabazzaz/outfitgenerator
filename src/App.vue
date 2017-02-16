<template>
  <div id="app">
    <hello></hello>
    <selected></selected>
    <tops></tops>
    <bottoms></bottoms>
    <shoes></shoes>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Selected from './components/Selected'
import Tops from './components/Tops'
import Bottoms from './components/Bottoms'
import Shoes from './components/Shoes'

export default {
  name: 'app',
  components: {
    Hello,
    Selected,
    Tops,
    Bottoms,
    Shoes
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
