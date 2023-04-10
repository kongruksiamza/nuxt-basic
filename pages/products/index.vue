<template>
    <div class="container">
        <div v-for="product in data.products">
            <NuxtLink :to="`/products/${product.id}`">
                <h2 class="title">{{ product.title }}</h2>
            </NuxtLink>
            <img :src=product.thumbnail>
        </div>
    </div>
</template>
<script setup>
useHead({
    title: "KongShop | สินค้าทั้งหมด",
    meta: [
        { name: "description", content: "ร้านค้า,อุปกรณ์คอมพิวเตอร์,เสื้อผ้า" }
    ]
})
const { data: data } = await useFetch('https://dummyjson.com/products?limit=12')
</script>

<style scoped>
.container{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.container div{
    width: 300px;
    height: 300px;
    margin: 30px 15px;
    background: #333;
}
.title{
    color: white;
    text-align: center;
    font-size: 1.2em;
}
.container div:hover{
    background: orange;
}
img{
    width: 300px;
    height: 300px;
}
a{
    text-decoration: none;
}
</style>