<script setup>
import { ref } from 'vue';
import Promotion from './components/promotion.vue';
import Category from './components/category.vue';

const categories = ref([
        {
            id: 0,
            name: 'Cake & Milk',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/8370/e915/8a586f746c0b10b70cd405c8aa1f2038?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=hD63Y9J-BDi3iSwmZSxDJtywiOiqiNs7rXm1jqMVvGxTOnp5GkAHDkKXEAbcQgb3SP8t8g~rJ9-TD5CpEUcVIk1xXCjEIvQZ0IjO0JJy3aDX2F42igACmCIwepdTjjYXu7b79rtSJt-ezKpN5uHo~spZNhS1liH-quvZuKlaee~8XGVaU97fy~XTHNgstqRwB~Qu8YqY3InUwDSQQaQIrWRKGgLL57Ns3xdbEFWkEj~G3tGCoWfwV5p8h4huK9g9jxf4PXROAskeix3Yg3BLXo-zyxomUdUlDOkADu6Nl-hk2JCotGtC6Q2sggnBfZfGv8R2pJReiI2teEUoyKyOYw__',
            quantity: 14,
            color : "bg-lime-200",
        },
        {
            id: 1,
            name: 'Peach',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/fa19/6bce/6720167ebdfcf5d3f8a2d76053176f9a?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=A4lft8Sys0Rp0fz3NTlq5GIJsDJdpRZsIEbW~Jg8rTlYnjw15SSl57xPB~HiLssubgj-QkMT574VVPr-7ze4XHynCF7qv0REbpuc1T1SlngVhGzKuFUviHrC6jUtwIT0ZJrWfselJzDlv7Mrj5crFT7Q9yo2mMRXr8JBmRCxmEvp07VMvDTZc-wrM1-7F3PSqD10hgHN9-mXQp7jTxBX64vltD-sYaJJR3JtOOA3sg73lKQ3avz7PZoPSWbOB8VryWmsC4rDsvkyIHT7MyM79tFYETVUME~0QaR8LpqPk3tSTwFjcciqiBEzttWsZg0zY6jnwtMkqh630W0FQtuPrw__',
            quantity: 17,
            color : "bg-rose-300",
        },
        {
            id: 2,
            name: 'kiwi',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/eb0a/46d6/bf3d30616b8cd69f4b03064fe254350c?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=fCBE7RZCCCprtO1akcEBrm4NteT2GsB66cZBYLwikZNOlPqdt-0T2GpKd9wE6CSCpvoo9nrHgxXDrfrr9kv1sk1qty2WQ8cguO09f5vdyb9E41ks5dMURQTHtu2Ok4IVSuJAhiOfJXbTtFrBgQZy4QIhpbSLSi4gBhIDkFIhxvxJDrS5raaBijgDszynoWtNIOwW15qOAIE6YYxmhG0BzWPXLa4VgrYqjawh2UF9JnekfiK04YgP0g6rP4VbmCA0qaKCjLel1PM5bsnes6~dMMeyLPBqsqLwVwS6Ipgy9iLa0IcS9EEA9a4~hmTcKK9k4J1ibB3MspTcoA-9i67kiQ__',
            quantity: 21,
            color : "bg-red-200",
        },
        {
            id: 3,
            name: 'Red apple',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/21b6/3a1e/f2a493eea176934bcab372692ab59a29?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=hZf-~FCqU7SvEx0AwlicGQO6M95e59Jwg5J3Er0EOrp7XiUl~GrGpla0IX3CFmZZQHdQW5-E0m7G7wsCVeEuj2XF9Tz8xhszSUANS2VZmn3RjNb2O7ud7nS3IzNYBTtZ5wLf6QdLZly7DvJc5JZMEwmSxHMSByGkjleUpSBNNJkWcRvI6fLpgqeCef5qBY63HaTKGlFazWS3Y6kzy9TfUiX3ZmlQqBttodi3tmbjS1hWfMsLc0rqh9l6HDaC2pZycQxQK7CbdDdYygCBbOjopqSHR4kUi02M7RdWQNyN4xAVSWUI4g-ZaI8tBAOCKK4eI5T-1TYkzb~1rI0NIZcBbA__',
            quantity: 68,
            color : "bg-orange-200", 
        
        },
        {
            id: 4,
            name: 'Snack',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/488c/b40d/98f6efd89c2347f8ab7f23b7757a7e2f?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=hxvVVqjkzKJzw6zevj3JoT1dox~2dWP2gUYNBpMg6VqXUhVdiM7tKgvOZUJCBwkZyyhDPfXV56gFM6MN9Kv~831Xq5-CcXbap2AQg9clujO1na2Cqbvi9y-J7axw6EaUi1DSR2g6LQN0mfLjofBYQ0~Mr9Vv3l6OI4M9SasuYXILCGDSDr~DZk-naM1oa77OiPg9dnvpDKBFt6pNy~Wpojj7tEspkgc0g4CXifj8NZn4qcer08xnA5bxoTH--lsbROFewIluHGiUZQfRr-xyl1pxcl9mPhzALzhcqb5vLgJwl8PGpEtLVtQrhKObycQgP17eFfWOV0Ok~7C69Dtb1g__',
            quantity: 34,
            color : "bg-amber-200",
        },
        {
            id: 5,
            name: 'Black plum',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/13f9/afc8/02816b515e817bcd88800c49b947f860?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=Ly3VtPyuFdvJBEfLG4j~NMQSVim7GRBPG2FuAEeqt1-q3N1JLZcLifWsMdjELuzllv~1HVkU1-geIL2LVgEiHOkMmv7pEPeeXG-xCfOH8v0~od4~gSS39AfJwx3sIE5y1fG2NBcFl6687j0XErBhdCETfucgXtu84zxaWIZ5LLOVNE6c8J9oM9322U7qc-Ztq5hq2MVE6bEKoKLTsks-vPNEMXH8Y9h5t4LSPFuH5r6u99YTknlG4~Z6LX3vWXv67WPmuwYPAA22MhKXdhYREA0nyVlIc~kdmJjobsdJixEyVfV5MNe3jMBKxfvg4-3uSP2J07OonCvrarMUaE9ESQ__',
            quantity: 25,
            color : "bg-yellow-200",
        },
        {
            id: 6,
            name: 'vegetable',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/5e6d/35bc/cc6f73e5412576546dca6b013f4fc9c7?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=Rl88YNpvdbd3Ntgs3Wg~Vw1X5nuzSPlxWmBF9nieUlNpSYYTtE6Hj0k1vtKKLVjRFKhSgvmHyE9uCDCel~mk6Ant7umRKDhbZniZOPhiU~AnAILMcXe8AnFd4QMHcVIxfXFwULsBgczhlj71Y7Gk89pLlbqqGuiEmVAuQA~wX5UZDekUX7sHWUK2wuTLokfqa0xLZzyMppOXlhaiKkcNeCXkosSGdOGPmnvf3UPT5GIb0TdAzisYBkOKzhE-1K-7Abjy1DDdgPNrh2EN6lLc0jnWjoVYzNZbYQqZLOOGg3zVdTr7DouvH4UI7iIKpLiCyKg6rGHs6a0CMtjO1Lmb~A__',
            quantity: 65,
            color : "bg-green-200",
        },
        {
            id: 7,
            name: 'Headphone',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/0ed9/44fa/3bcccc269ae2cadb2fb25ac9b02ea29e?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=aPOGlxc6IHGbPdHUt5t6eVG3OGIm5UmXBNyQ-FLR9w7TDsEInyQBg2kfJSwm8xuVH1mf-~SNLdImAM1lWAsSE3PGJ~l65YiLJpZnegqTIwnCxqB879NXZJujqPQ-r90jr9LDnVEVYNuVApneVuNx79~mpxHm4wlRzK3fFcLgngnOKoyFcnLS6HjsCWL1bkS4V9EtxR2ryQIQNJLX3gpDBvKBOrYwXqmU4lnuWO8bZPuWRmI5rW0SQXEseTz-UpjKKn4OMrRuNxNbet8GACDOs0deSUXLB-NM8YP5CWi82F-kdcRotYO5dRq5p-TsyOWLKFVRKQwgGI-Zw46ySKisJQ__',
            quantity: 33,
            color : "bg-emerald-200",
        },
        {
            id: 8,
            name: 'Cake & Milk',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/78c4/8886/688817c7c490b88407c4904743141184?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=SIM2GHPExFto3CSSkLnHRtNqxKIyqWbjHzQ-6JtMDjmE4II37oKdqHHX4bz7J4~4NUVM80TMoJS-T6Ubd6mGNiST1UnS0Fxjfi7fl8pHX8IoVgiTwngU61iZvxolB4b5X7msaO52nH0M6Un~swWfMn8zQbrOxVs6hxAJ0C6ReJnuOAJGfwc5bh2q95fcl5PMoXKJwEXWItcI5D06shSEEW6gatpSN~bSh9anLni~J-Rl9DZdITqbSHJUM3JnLrbzrK56tT0hirxDFJyZjzvJlBPI8aLDJCTTuaOFX-pXv6HJypkX36Gti2ZI1GgE-mixJA7Kncxmyk~CLB~FGCNhPA__',
            quantity: 55,
            color : "bg-teal-200",
        },
        {
            id: 9,
            name: 'orange',
            imageUrl: 'https://s3-alpha-sig.figma.com/img/aadc/a20d/2ca905cbdfec3bf306fbe70e1ca34a8a?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=eDyikxNXW~CaK0F6pgC9foSL2z5y-RFaMrqg9CmtuN4a9sQNn0E6DAdAW-wwGZ8YsAWyGnsNXaAHBq96rJDlTLWOt7JTG4m3z-QyV7wdJ54jc0nISgPXhnRmit3TsOWZhIbyj0qF9SS3nD-yVPW4df4uaK41CPcLVUANOeQwPV~YBXrHQZ-OF9cRHN3iOLYolsdVkLh-8HMlppqneAXHXnJ18eieTeGQJzfsnAMMMF8PhWr6yiDrIPJH5CDue7lsCKsYvBRqbFn20X2QWV89u292azleYkivco-nymEUvksuw1PI4ZFPGOpnCWmYKbunCuuhzMBtUT~4aHJQ2LaSBg__',
            quantity: 63,
            color : "bg-cyan-200",
        },
    ]);
</script>
  
<template>
     <div class="bg-white mb-10">
        <ul role="list" class="mx-auto mt-20 grid max-w-2xl grid-cols-1 gap-x-2 gap-y-2 sm:grid-cols-1 lg:mx-0 lg:max-w-none lg:grid-cols-10">
            <Category
            v-for="item in categories"
            :category="item"
            :key="item.id"
          >
            </Category>
        </ul>
    </div>
    <div class="mx-auto mt-20 grid max-w-2xl grid-cols-1 gap-x-2 gap-y-2 sm:grid-cols-1 lg:mx-0 lg:max-w-none lg:grid-cols-3">
        <Promotion />
    </div>
</template>