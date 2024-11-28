<template>
  <div class="container"
            style="border-radius: 4px; background-color: rgb(97, 181, 130); width: 80px; text-align: center; color: white">
            <button @click="shopNow + promotion.title">Shop Now</button>
          </div>
</template>

<script>
export default {
  props: {
    title: String,
  },
  methods: {
    shopNow() {
      alert(`Let's shop ${this.message}`);
    },
  },
};
</script>
