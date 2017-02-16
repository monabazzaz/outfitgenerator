<template>
  <div class="container-fluid">
    <div class="selected">
      <div class="row">
        <div class="col-lg-3 upper">
          <h2> {{ msg }} </h2>
          <div class="box"></div>
        </div>
        <div class="col-lg-3 lower">
          <h2> {{ mng }} </h2>
          <div class="box"></div>
        </div>
        <div class="col-lg-3 feet">
          <h2> {{ mpg }} </h2>
          <div class="box"></div>
        </div>
        <div class="col-lg-3 combined">
          <h2> {{ mdg }} </h2>
          <div class="box"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'selected',
  data () {
    return {
      msg: 'SELECTED TOP',
      mng: 'SELECTED BOTTOMS',
      mpg: 'SELECTED SHOES',
      mdg: 'COMPLETE OUTFIT'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2 {
  font-family: 'Londrina Outline', cursive;
  color: #647ea8;
  font-size: 2em;
}

.upper {
  display: inline-block;
  text-align: center;
  padding: 0 40px 0 40px;
}

.box {
  flex-basis: 30%;
  height: 100px;
  border: 1px solid #9a9a9a;
  border-radius: 4px;
  overflow: hidden;
}

.lower {
  display: inline-block;
  text-align: center;
  padding: 0 40px 0 40px;
}

.feet {
  display: inline-block;
  text-align: center;
  padding: 0 40px 0 40px;
}

.combined {
  display: inline-block;
  text-align: center;
  padding: 0 40px 0 40px;
}
</style>
