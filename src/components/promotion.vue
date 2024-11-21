<template>
  <div class="promotion_card grid grid-rows-3 grid-flow-col gap-4" style="background-color: rgba(231, 234, 243, 1);">
    <div class=" text-content row-span-2 col-span-2 ">
      <h3>{{ title }}</h3>
      <div class="container" style="border-radius: 4px; background-color: rgb(97, 181, 130); width: 80px; text-align: center; color: white"><button @click="shopNow">Shop Now</button></div> 
    </div>
    <div class="row-span-3 col-span-3 ">
      <img :src="image" alt="promotion Image" style="height: 100px; width: 250px;"/>
    </div>    
  </div>

</template>

<script>
export default {
  props: ["title", "image"],
  methods:{
    shopNow(){
      alert(`Let' shop ${this.title}
      `);
    }
  }
}
</script>

<style scoped>
.promotion_card {
  display: flex;
  align-items: center;
  padding: 20px;
  border-radius: 10px;
}

.promotion_card img {
  width: 100px;
  height: 120px;
  object-fit:inherit;
}

.text-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.text-content h3 {
  font-size: 18px;
  color: blue;
  margin-bottom: 8px;
}

</style>

