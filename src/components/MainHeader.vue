<template>
   
    <img 
    class="profile-image" 
    :src="require('@/assets/profilbild_enrico_carruba2.png')" 
    alt="Enrico Carruba">
   
    <h1>Hello, my name is <br> <span> Enrico Carruba</span></h1>
    <p>I am a passionate junior <span> Web and Software Developer.</span></p>
    <p class="welcome-text">Welcome to my digital CV and portfolio page! Feel free to contact me.</p>
</template>
<script>
export default {
    
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Sora:wght@100;200;300;400;500;600;700;800&display=swap');
html {
    font-family: 'Sora';  
    margin: 1rem; 
}

h1{
    font-weight: 300;
}

h1 span{
    font-weight: 600;
}

h2{
    
    text-align: center;
}

.profile-image {
    width: 80%;
    border-radius: 50%;
}

p {
    
    font-weight: 400;
    margin: 1.5rem;
}

p span {
    display: block;
    font-weight: bolder;
}

.welcome-text{
    text-align: justify-all;
}

</style>

