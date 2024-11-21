<template>
    <li :key="category.id"> 
      <div :style="{ textAlign: 'center', borderRadius: '16px' }" :class="category.color">
        <img class="mx-auto h-450 w-450 square-full" :src="category.imageUrl" alt="Category Image" />
        <p class="text-sm leading-2 mt-5 text-gray-800">{{ category.name }}</p>
        <p style="text-decoration: color(rgba(182, 182, 182, 1));">{{ category.quantity }} Items</p> 
      </div>
    </li>
  </template>
  
  <script setup>
  defineProps({
    category: {
      type: Object,
      required: true,
    },
  });
  </script>
  