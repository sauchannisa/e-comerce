<template>
  <div :style="{ backgroundColor: color }" class="product-category">
    <img :src="image" :alt="name" style="width: 100px; height: 100px;" />
    <h3>{{ name }}</h3>
    <p>{{ count }} items</p>
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    name: String,
    count: Number,
    color: String,
  },
};
</script>

<style>
.product-category {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 140px;
  padding: 10px;
  background-color: #f0f2f5;
  border-radius: 10px;
  margin: 10px;
  cursor: pointer;
}
</style>
