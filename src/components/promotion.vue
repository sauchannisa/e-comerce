<script>
import Button from './button.vue';

</script>
<template>
  <div class="promotion_card grid grid-rows-3 grid-flow-col gap-4" style="background-color: rgb(239, 232, 214);">
    <div class=" text-content row-span-2 col-span-2 ">
      <h3>Everyday Fresh & Clean with Our Products</h3>
      <div class="container" style="border-radius: 4px; background-color: rgb(97, 181, 130); width: 80px; text-align: center; color: white"><button>Shop Now</button></div> 
    </div>
    <div class="row-span-3 col-span-3 ">
      <img src="https://s3-alpha-sig.figma.com/img/de8c/488a/87b9ce16acd7436a6dec758331c840bc?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=eBaGoY030QP90fBRwlcsx9~1AGCuFC89E9fzmdCM71JghJVImUZ4JKtMyqd9E4RqtVFZ~VFqGFpi1mdSbCF~Tx9Qo9DRfPQCK4kOp2u6Xl7xC7pusoYKK-y3fMhDW28mYW1wM99FCfMJb5QVJtYwlmAvb9NCkOjGWeLvzBD2hNAUaI4eGt47WaScgbYgFMtlfHMVXkcJ06bECFFlsYXQv3MOHxmJdudBjuRAfk9VyqwaPPGmhRMPcyAtOu4hNmngyA71O2xVdf2LBr~OPf9CqGTHiJ9UeX1qFa7lK9HQWbwszFZgQcnrQ1sLxRa6eGNPXb-4XdVv-JRnQQmY7RD55A__" alt="promotion Image" style="height: 100px; width: 250px;"/>
    </div>    
  </div>

  <div class="promotion_card grid grid-rows-3 grid-flow-col gap-4" style="background-color: rgb(241, 232, 232);">
    <div class=" text-content row-span-2 col-span-2 ">
      <h3>Make your Breakfast Healthy and Easy</h3>
      <div class="container" style="border-radius: 4px; background-color: rgb(97, 181, 130); width: 80px; text-align: center; color: white"><button>Shop Now</button></div> 
    </div>
    <div class="row-span-3 col-span-3 ">
      <img src="https://s3-alpha-sig.figma.com/img/2738/f29f/1c4542246febe8c91ddb74ce42b81c5d?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=k68UmrSBWC8jSRnbsQsKTe5Gc19E5fFQcMtYAA4vW0NAwOeKS2HnnCqd4JadZgLPsWlGfHjyyAPUwP5z74ypYuQm7lGffz2iFZRWMynbu8dM8IAACGwh5xsH-Okx0ZbkmTnTA0jWjYwh6L6u5h185DSML5dQ~3cwr-BqTR1tbFRblzSG7dzRQHtXx1Tq-NOmgv4MCnrBWRV8a5rFVqYCWu0qW8i~553cHoMBsbk1Hr15wjAStgnRn0GFa-MKRbO9fZdLTAbJ-VwbkrbgG2AxMkWacfSg12wKaOcT-13X1b6JXjv0w6JO05hE3Vg77I2rrlvkXVpQv0H-tY3w3MjO8w__" alt="promotion Image" />
    </div>
  </div> 
  <div class="promotion_card grid grid-rows-3 grid-flow-col gap-4" style="background-color: rgb(231, 234, 242);">
    <div class="text-content row-span-2 col-span-2 ">
      <h3>The best Organic Products Online</h3>
      <div class="container" style="border-radius: 4px; background-color: rgb(97, 181, 130); width: 80px; text-align: center; color: white"><button>Shop Now</button></div> 
    </div>
    <div class="row-span-3 col-span-3 ">
        <img src="https://s3-alpha-sig.figma.com/img/4d69/6151/8879bc373bf5fcc1578bcec5172b087b?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=dc7wBR4CRNv8A5hVXVclm0zDidMgHnSN9gM0nV9i~jPh6iZEpvEuhJqFzxw8sjo8tMRIHvcnMYx3GtPEAX~rg9BwP1PTpFz69qblO3QNt0wGYwTKUSaP-ULJcjKvDG78U1DpaiPol1pEo9ZG7YwZFNmuH4Ga8lHQ6Kbbb6YG4wAAer~66KRSwx0Jw1Rm~532E~L1amY5tnribs1KofbLS~GN3UAh~kPoZf6jTlePzc-LZigzJo8pwXxjQ0zzQ6rGbwXcXCk1uc8YQsIsPqr0H66jaU5BhtYCYSjhRzVcIOxfqNafk91557kRQrK2s~ajDZkql872Zh81e1pH8yHX7A__" alt="promotion Image" />
    </div>
  </div>
</template>

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

