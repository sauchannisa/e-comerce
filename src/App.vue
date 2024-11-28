<script setup>
import { ref } from 'vue';

import PromotionComponent from './components/PromotionComponent.vue';
import CategoryComponent from './components/CategoryComponent.vue';

</script>

<template>
  <div class="bg-white mb-10">
    <ul role="list"
      class="mx-auto mt-20 grid max-w-2xl grid-cols-1 gap-x-2 gap-y-2 sm:grid-cols-1 lg:mx-0 lg:max-w-none lg:grid-cols-10">
      <CategoryComponent />
    </ul>
    <div
      class="mx-auto mt-20 grid max-w-2xl grid-cols-1 gap-x-2 gap-y-2 sm:grid-cols-1 lg:mx-0 lg:max-w-none lg:grid-cols-3">
      <PromotionComponent />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {
    fetchCategories() {
      // Your axios call goes here
      axios.get('http://localhost:3000/api/categories')
        .then(response => {
          console.log(response.data); // Access the data
          this.categories = response.data;
        })
        .catch(error => {
          console.error('Error fetching data:', error);
        });
    },
    fetchPromotions() {
      // Your axios call goes here
      axios.get('http://localhost:3000/api/promotions')
        .then(response => {
          console.log(response.data); // Access the data
          this.promotions = response.data;
        })
        .catch(error => {
          console.error('Error fetching data:', error);
        });
    }
  },
  mounted() {
    // Mounted life cycle - It will be executed every time
    // this component is loaded
    this.fetchCategories()
    this.fetchPromotions()
  }
}

</script>