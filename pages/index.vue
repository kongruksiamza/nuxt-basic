<template>
    <div class="container">
        <h1>หน้าแรกของเว็บไซต์</h1>
        <img src="/image/shopping.svg">
    </div>
</template>
<script setup>
useHead({
    title: "KongShop | หน้าแรกของเว็บไซต์",
    meta: [
        { name: "description", content: "ร้านค้า,อุปกรณ์คอมพิวเตอร์,เสื้อผ้า" }
    ]
})
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

img {
    width: 500px;
    height: 500px;
}
</style>