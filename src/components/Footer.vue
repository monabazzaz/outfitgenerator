<template>
  <div class="footer">
    <h2> {{ msg }} </h2>
  </div>
</template>

<script>
export default {
  name: 'footer',
  data () {
    return {
      msg: 'This project was made possible thanks to the help of my amazing roommate, Martha Carter, and the fact that she took pictures of 125 outfit cominations without complaint. For a look at more of my work, please take a peek at my online portfolio which is located <a href="monabazzaz.org/portfolio">here</a>. Cheers!'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h2 {
  font-family: 'Nixie One', cursive;
  text-align: center;
  font-size: 2em;
  color: #4b4c4f;
}
</style>
