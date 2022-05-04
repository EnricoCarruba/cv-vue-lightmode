<template>
    <h1>My current stack:</h1>
    <div class="stack-images-container">
    <img class="stack-images" :src="require('@/assets/HTML5.png')" alt="">
    <img class="stack-images" :src="require('@/assets/css.png')" alt="">
    <img class="stack-images" :src="require('@/assets/javascript.png')" alt="">
    <img class="stack-images" :src="require('@/assets/node.png')" alt="">
    <img class="stack-images" :src="require('@/assets/npm.png')" alt="">
    <img class="stack-images" :src="require('@/assets/java.png')" alt="">
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
.stack-images-container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    align-items: center;
    
   
   
}

.stack-images {
    width: 20vw;
}
</style>