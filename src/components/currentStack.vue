<template>
    <div class="stack-component-container">
        <h3>My stack</h3>
        <div class="stack-images-container">
            <img class="stack-images" :src="require('@/assets/HTML5.png')" alt="">
            <img class="stack-images" :src="require('@/assets/css.png')" alt="">
            <img class="stack-images" :src="require('@/assets/javascript.png')" alt="">
            <img class="stack-images" :src="require('@/assets/node.png')" alt="">
            <img class="stack-images" :src="require('@/assets/npm.png')" alt="">
            <img class="stack-images" :src="require('@/assets/java.png')" alt="">
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
.stack-component-container{
    width: 90vw;
    height: 45vh;
    margin: 1rem;
    box-shadow: 0px 0px 25px lightgrey;
}

h3 {
    margin: 1rem;
    padding-top: 1rem;
    color: gray;
    
}

.stack-images-container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    
   
}

.stack-images {
    width: 100px;
    height: 100px;
    object-fit: contain;
    justify-self: center;
    align-self: center;
    
}
</style>