<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Hello! Today is {{ date }} Welcome to this customized outfit generator.</h2>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'WHAT TO WEAR TODAY?',
      date: Date()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-family: 'Londrina Outline', cursive;
  text-align: center;
  color: #647ea8;
  font-size: 3em;
}

h2 {
  font-family: 'Nixie One', cursive;
  text-align: center;
  font-size: 1em;
  color: #4b4c4f;
}
</style>
