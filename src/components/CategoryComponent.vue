<template>
  <ul v-for="category in categories" :key="category.id">
    <li>
      <div :style="{ textAlign: 'center', borderRadius: '16px',background: category.color}">
        <img class="mx-auto h-450 w-450 square-full" :src="'http://localhost:3000/' + category.image" alt="Category Image" />
        <p class="text-sm leading-2 mt-5 text-gray-800">{{ category.name }}</p>
        <p style="color: grey;">{{ category.productCount }} Items</p>
      </div>
    </li>
  </ul>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      categories: [] // Initialize an empty array to store categories
    };
  },

  mounted() {
    // Fetch data from the API when the component is mounted
    axios
      .get('http://localhost:3000/api/categories') // Ensure correct protocol (http://)
      .then(response => {
        this.categories = response.data; // Set the categories array to the response data
      })
      .catch(error => {
        console.error('There was an error fetching the categories:', error);
      });
  },
};
</script>
