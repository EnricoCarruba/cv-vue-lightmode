<template>
    <div class="footer-container">
            <div class="call">
                <img :src="require('@/assets/phone.svg')" alt="call"/>
                <span>+49 151 288 026 29</span>
            </div>
        
        <div class="mail">
            <img :src="require('@/assets/email.svg')" alt="call"/>
            <span>carrubaenrico@gmail.com</span>
        </div>
        <!-- <div class="download">
            <img :src="require('@/assets/download.svg')" alt="call"/>
            <span>Download CV</span>
        </div> -->
    </div>
</template>

<script>
export default {
    
}
</script>

<style>

.footer-container {
    background-color: lightsalmon;
    display: grid;
    grid-template-columns: 1fr 1fr;
   
    font-size: 0.75rem;
}

img{
    height: 10vh;
    width: 10vw;
    
}

</style>