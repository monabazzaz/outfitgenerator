<template>
  <div class="container-fluid">
    <div class="tops">
      <div class="row">
        <div class="col-lg-3 col-md-6 col-sm-12 upper">
          <h2> {{ msg }} </h2>
          <div class="box" v-for="top in tops">
            <a href="#"><img :src="top.img" @click="selectedTop(top)"></a>
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
      tops: [
        {
          title: 'Top 1',
          key: 'adidas',
          img: '/static/images/T1.jpg'
        },
        {
          title: 'Top 2',
          key: 'hm',
          img: '/static/images/T2.jpg'
        },
        {
          title: 'Top 3',
          key: 'zara',
          img: '/static/images/T3.jpg'
        },
        {
          title: 'Top 4',
          key: 'dakota',
          img: '/static/images/T4.jpg'
        },
        {
          title: 'Top 5',
          key: 'brandy',
          img: '/static/images/T5.jpg'
        }
      ],
      msg: 'Start: Select a top!'
    }
  },
  methods: {
    selectedTop: function (top) {
      console.log(top)
      this.$emit('selected', top)
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
