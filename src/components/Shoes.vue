<template>
  <div class="container-fluid">
    <div class="shoes">
      <div class="row">
        <div class="col-lg-3">
        </div>
        <div class="col-lg-3">
        </div>
        <div class="col-lg-3 feet">
          <h2> {{ msg }} </h2>
          <div class="box" v-for="shoe in shoes">
            <a href="#"><img :src="shoe.img" @click="selectedShoe(shoe)"></a>
          </div>
        </div>
        <div class="col-lg-3">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'shoes',
  data () {
    return {
      shoes: [
        {
          title: 'Shoe 1',
          key: 'birks',
          img: '/static/images/S1.jpg'
        },
        {
          title: 'Shoe 2',
          key: 'sneaks',
          img: '/static/images/S2.jpg'
        },
        {
          title: 'Shoe 3',
          key: 'booties',
          img: '/static/images/S3.jpg'
        },
        {
          title: 'Shoe 4',
          key: 'docs',
          img: '/static/images/S4.jpg'
        },
        {
          title: 'Shoe 5',
          key: 'hunter',
          img: '/static/images/S5.jpg'
        }
      ],
      msg: 'Choose some shoes!'
    }
  },
  methods: {
    selectedShoe: function (shoe) {
      console.log(shoe)
      this.$emit('selected', shoe)
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

.feet {
  position: relative;
  float: left;
  width: 20%;
  left: 5%;
  /*padding: 0 40px 0 40px;*/
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

button {
  margin-top: 40px;
}

@media screen and (max-width: 1100px) {

.box {
  display: block;
  width:100%;
  text-align: left;
  margin: 20px 0 20px 0;
  height: 250px;
  width: 250px;
}

.feet {
  display: block;
  width:100%;
  left: 0%;
  text-align: left;
  padding-left: 10px;
}

}
</style>
