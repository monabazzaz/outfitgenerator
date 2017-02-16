<template>
  <div class="container-fluid">
    <div class="selected">
      <div class="row">
        <div class="col-lg-3 col-md-6 col-sm-12 upper">
          <h2> {{ msg }} </h2>
          <div class="box1"></div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12 lower">
          <h2> {{ mng }} </h2>
          <div class="box"></div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12 feet">
          <h2> {{ mpg }} </h2>
          <div class="box"></div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12 combined">
          <h2> {{ mdg }} </h2>
          <div class="box4"></div>
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
  text-align: center;
}

.upper {
  float: left; width: 23%;
  position: relative;
  display: inline-block;
  padding-left: 40px;
}

.box {
  flex-basis: 30%;
  height: 250px;
  width: 250px;
  border: 1px solid #647ea8;
  border-radius: 4px;
  overflow: hidden;
}

.box1 {
  flex-basis: 30%;
  height: 250px;
  width: 250px;
  border: 1px solid #647ea8;
  border-radius: 4px;
  overflow: hidden;
}

.box4 {
  flex-basis: 30%;
  height: 250px;
  width: 250px;
  border: 1px solid #647ea8;
  border-radius: 4px;
  overflow: hidden;
}

.lower {
  float: left; width: 23%;
  position: relative;
  display: inline-block;
}

.feet {
  float: left; width: 23%;
  position: relative;
  display: inline-block;
}

.combined {
  float: left; width: 23%;
  position: relative;
  display: inline-block;
  text-align: center;
}

@media screen and (max-width: 1100px) {

.upper {
  display: block;
  width:100%;
  text-align: left;
  padding-left: 10px;
}

.lower {
  display: block;
  width:100%;
  text-align: left;
  padding-left: 10px;
}

.feet {
  display: block;
  width:100%;
  text-align: left;
  padding-left: 10px;
}

.combined {
  display: block;
  width:100%;
  text-align: left;
  padding-left: 10px;
}

}
</style>
