<template>
  <div class="shoes">
    <div class="col-lg-3">
    </div>
    <div class="col-lg-3">
    </div>
    <div class="col-lg-3 feet">
      <h2> {{ msg }} </h2>
      <div class="box"></div>
      <div class="box"></div>
      <div class="box"></div>
      <div class="box"></div>
      <div class="box"></div>
    </div>
    <div class="col-lg-3">
    </div>
  </div>
</template>

<script>
export default {
  name: 'shoes',
  data () {
    return {
      msg: 'Please pick a pair of shoes!'
    }
  }
}
</script>


<style scoped>
h2 {
  padding-top: 20px;
  font-family: 'Nixie One', cursive;
  text-align: left;
}

.feet {
  padding: 0 40px 0 40px;
}

.box {
  flex-basis: 30%;
  height: 175px;
  width: 250px;
  border: 1px solid #9a9a9a;
  border-radius: 4px;
  overflow: hidden;
  margin: 40px 0 40px 0;
}
</style>
