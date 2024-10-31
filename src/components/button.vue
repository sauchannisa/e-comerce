<template>
  <div class="container" style="border-radius: 4px; background-color: rgb(97, 181, 130); width: 80px; text-align: center; color: white" v-on="shopNow"><button>Shop Now</button></div> 
</template>
<script >
export default {
  props: {
    message: String,
    

  },
  methods:{
    shopNow(){
      alert
      (`Let's shop ${this.message}`)
    }
  }
}
    
</script>