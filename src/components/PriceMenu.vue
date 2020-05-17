<template>
  <div>
    <div class="header">
      <span class="text"> Our Pricing </span> <br/> <br/> <br/>
      Annually
      <label class="switch">
        <input type="checkbox" ref="inputbutton" checked @click="buttontoggle" autofocus>
        <span class="slider round"> </span>
      </label>
      Monthly
    </div>

    <div class="gridcontiner">
      <div class="firstcontiner">
        <h3> Basic <br /> </h3>
        <h1 v-if="elementvisibility"> <span class="monthly"> <b> &dollar;19.99 </b> <br/> </span> </h1>
        <h1 v-else>  <span class="annually"> <b> &dollar;199.99 </b> <br/> </span > </h1>
        <hr>
        <h4> 500 GB Storage <br/> </h4>
        <hr>
        <h4> 2 Users Allowed <br/> </h4>
        <hr>
        <h4> Send up to 3 GB<br/> </h4>
        <hr> <br/>
        <button class="sidebutton" type="button"> Learn More </button>
      </div>

      <div class="middlecontiner">
        <h3> Professional <br /> </h3>
        <h1 v-if="elementvisibility"> <span class="monthly"> <b> &dollar;24.99 </b> <br/> </span> </h1>
        <h1 v-else> <span class="annually"> <b> &dollar;249.99 </b> <br/> </span> </h1>
        <hr>
        <h4> 1 TB Storage <br/> </h4>
        <hr>
        <h4> 5 Users Allowed <br/> </h4>
        <hr>
        <h4> Send up to 10 GB <br/> </h4>
        <hr> <br/>
        <button class="middlebutton" type="button"> Learn More </button>
      </div>

      <div class="lastcontiner">
        <h3> Master <br /> </h3>
        <h1 v-if="elementvisibility"> <span class="monthly"> <b> &dollar;39.99 </b> <br/> </span> </h1>
        <h1 v-else> <span class="annually"> <b> &dollar;399.99 </b> <br/> </span> </h1>
        <hr>
        <h4> 2 TB Storage <br/> </h4>
        <hr>
        <h4> 10 Users Allowed <br/> </h4>
        <hr>
        <h4> Send up to 20 GB <br/> </h4>
        <hr> <br/>
        <button class="sidebutton" type="button"> Learn More </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PriceMenu',
  data () {
    return {
      elementvisibility : true
    }
  },
  methods: {
    buttontoggle () {
            this.elementvisibility = !this.elementvisibility;
    } 
  }
}
</script>
