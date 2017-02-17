<template>
  <div class="container-fluid">
    <div class="selected">
      <div class="row">
        <div class="col-lg-3 col-md-6 col-sm-12 upper">
          <h2> {{ msg }} </h2>
          <div class="selectedTop">
            <img :src="top.img" v-if="top">
          </div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12 lower">
          <h2> {{ mng }} </h2>
          <div class="selectedBottom">
            <img :src="bottom.img" v-if="bottom">
          </div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12 feet">
          <h2> {{ mpg }} </h2>
          <div class="selectedShoe">
            <img :src="shoe.img" v-if="shoe">
          </div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12 combined">
          <h2> {{ mdg }} </h2>
          <div class="combinedOutfit">
            <img :src="currentOutfit" v-if="shoe && bottom && top">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {

  mounted () {
    console.log('Top Mounted')
    axios.get('/static/clothes.json')
      .then((response) => {
        console.log(response)
        this.outfits = response.data
      })
  },
  props: [
    'top',
    'bottom',
    'shoe'
  ],

  name: 'selected',
  data () {
    return {
      msg: 'SELECTED TOP',
      mng: 'SELECTED BOTTOMS',
      mpg: 'SELECTED SHOES',
      mdg: 'COMPLETE OUTFIT'
    }
  },
  computed: {
    currentOutfit () {
      this.outfits[this.bottom.key][this.shoe.key][this.top.key]
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

.selectedTop {
  flex-basis: 30%;
  height: 250px;
  width: 250px;
  border: 1px solid #647ea8;
  border-radius: 4px;
  overflow: hidden;
}

.selectedBottom {
  flex-basis: 30%;
  height: 250px;
  width: 250px;
  border: 1px solid #647ea8;
  border-radius: 4px;
  overflow: hidden;
}

.selectedShoe {
  flex-basis: 30%;
  height: 250px;
  width: 250px;
  border: 1px solid #647ea8;
  border-radius: 4px;
  overflow: hidden;
}

.combinedOutfit {
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
