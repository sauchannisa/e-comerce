<template>
    <li :key="category.id"> 
      <div :style="{ textAlign: 'center', borderRadius: '16px' }" :class="category.color">
        <img class="mx-auto h-450 w-450 square-full" :src="category.imageUrl" alt="" />
            <p class="text-sm leading-2 mt-5 text-gray-800">{{ category.name }}</p>
            <ul role="list" class="mt-2 flex justify-center gap-x-1">
              <p style="text-decoration: color(rgba(182, 182, 182, 1));">{{ productCount }} Items</p> 
            </ul>
          
        </div> 
    </li>      
</template>
  
<script setup>
    const props = defineProps ({
        pros: {
            color: String,
            productCount: String,
            name: String,
            imageUrl: String,
        },
    })
</script>