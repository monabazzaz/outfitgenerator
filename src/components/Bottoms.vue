<template>
  <div class="container-fluid">
    <div class="bottoms">
      <div class="row">
        <div class="col-lg-3">
        </div>
        <div class="col-lg-3 lower">
          <h2> {{ msg }} </h2>
          <div class="box" v-for="bottom in bottoms">
            <a href="#"><img :src="bottom.img" @click="selectedBottom(bottom)"></a>
          </div>
        </div>
        <div class="col-lg-3">
        </div>
        <div class="col-lg-3">
        </div>
      </div>
    <div>
  </div>
</template>

<script>
export default {
  name: 'bottoms',
  data () {
    return {
      bottoms: [
        {
          title: 'Bottom 1',
          key: 'skirt',
          img: '/static/images/B1.jpg'
        },
        {
          title: 'Bottom 2',
          key: 'shorts',
          img: '/static/images/B2.jpg'
        },
        {
          title: 'Bottom 3',
          key: 'leggings',
          img: '/static/images/B3.jpg'
        },
        {
          title: 'Bottom 4',
          key: 'jorts',
          img: '/static/images/B4.jpg'
        },
        {
          title: 'Bottom 5',
          key: 'jeans',
          img: '/static/images/B5.jpg'
        }
      ],
      msg: 'Pick some bottoms!'
    }
  },
  methods: {
    selectedBottom: function (bottom) {
      console.log(bottom)
      this.$emit('selected', bottom)
    }
  }
}
</script>


<style scoped>
h2 {
  padding-top: 20px;
  font-family: 'Nixie One', cursive;
  text-align: center;
}

.lower {
  position: relative;
  float: left;
  width: 20%;
  left: 2.5%;
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

.lower {
  display: block;
  width:100%;
  left: 0%;
  text-align: left;
  padding-left: 10px;
}

}
</style>
