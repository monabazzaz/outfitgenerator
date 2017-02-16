<template>
  <div class="container-fluid">
    <div class="tops">
      <div class="row">
        <div class="col-lg-3 col-md-6 col-sm-12 upper">
          <h2> {{ msg }} </h2>
          <div class="box">
            <img :src="imgSrc">
          </div>
          <div class="box">
            <img :src="iSrc">
          </div>
          <div class="box">
            <img :src="imSrc">
          </div>
          <div class="box">
            <img :src="imSr">
          </div>
          <div class="box">
            <img :src="imageSrc">
          </div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12">
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12">
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'tops',
  data () {
    return {
      msg: 'Start: Pick a top!',
      imgSrc: '/static/images/T1.JPG',
      iSrc: '/static/images/T2.JPG',
      imSrc: '/static/images/T3.JPG',
      imSr: '/static/images/T4.JPG',
      imageSrc: '/static/images/T5.JPG'
    }
  }
}
</script>


<style scoped>
h2 {
  font-family: 'Nixie One', cursive;
  text-align: center;
  padding-top: 20px;
}

.upper {
  padding-left: 40px;
  float: left; width: 20%;
  position: relative;
}

.box {
  flex-basis: 30%;
  height: 250px;
  width: 250px;
  border: 1px solid #647ea8;
  border-radius: 4px;
  overflow: hidden;
  margin: 40px 0 40px 0;
}

.box:hover {
  background: rgba(115, 152, 183, 0.4);
  cursor: pointer;
}

img {
  opacity: 1.0;
  transition: opacity 1s ease-in-out;
  -moz-transition: opacity 1s ease-in-out;
  -webkit-transition: opacity 1s ease-in-out;
}
img:hover {
  opacity: 0.6;
  transition: opacity .55s ease-in-out;
  -moz-transition: opacity .55s ease-in-out;
  -webkit-transition: opacity .55s ease-in-out;
}​

@media screen and (max-width: 1100px) {

.box {
  display: block;
  width:100%;
  text-align: left;
  margin: 20px 0 20px 0;
  height: 250px;
  width: 250px;
}

.upper {
  display: block;
  width:100%;
  text-align: left;
  padding-left: 10px;
}

}
</style>
