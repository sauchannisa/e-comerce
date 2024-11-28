<template>
  <ul v-for="promotion in promotions" :key="promotion.id">
    <li :key="promotion.id">
      <div class="promotion_card grid grid-rows-3 grid-flow-col gap-4"
        style="background-color: rgba(231, 234, 243, 1);">
        <div class="text-content row-span-2 col-span-2">
          <h3>{{ promotion.title }}</h3>
          <div class="container"
            style="border-radius: 4px; background-color: rgb(97, 181, 130); width: 80px; text-align: center; color: white">
            <button @click="shopNow(promotion.title) ">Shop Now</button>
          </div>
        </div>
        <div class="row-span-3 col-span-3">
          <img :src= "promotion.image" alt="Promotion Image" style="height: 100px; width: 250px;" />
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  methods: {
    shopNow(title){
      alert(`Let's shop ` + title);
    },
  },
  data() {
    return {
      promotions: [
        {
          id: 1,
          title: "Everyday Fresh & Clean with Our Products",
          image: "https://clipart-library.com/image_gallery2/Onion-PNG-File.png",
        },

        {
          id: 2,
          title: "Make your Breakfast Healthy and Easy",
          image: "https://s3-alpha-sig.figma.com/img/2738/f29f/1c4542246febe8c91ddb74ce42b81c5d?Expires=1733702400&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=kCzGwtUVHFUoe36bfN0v6N8SmOKmCyj6PQNJJmGRxE770ORk1Oo0k8LgJ9of~qmBhSoH9SPkyo3LBu2HRdDmgrke7Vzk9FFBJ1mI9i8QYBE-qtigZGaw6cvh4MgUTQ8yzwgrQnjLCR4soII9OX9OLtUwSLoSh6N0kok3~IQdyf6QQA8jgOGr~d5YSn2r-JIGlaGycS3C1RipXCrTGRtcaBPTqClTNBXHwmJy8tep4wkORc4rdai5hdvGXa6KOCjITmbIfCp0JZwCpYH4eiUlDh8RAvrmLYBRU6-gL1YbLEzknHBbENLcxb70db-nsq2VrJdVtIN22EM1-BE6UI4oYg__",
        },
        {
          id: 3,
          title: "Make your Breakfast Healthy and Easy",
          image: "./src/assets/vegetable.jpg",
        }
      ]
    }
  }
};
</script>

<style scoped>
.promotion_card {
  display: flex;
  align-items: center;
  padding: 20px;
  border-radius: 10px;
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
