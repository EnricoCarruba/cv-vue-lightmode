<template>
    <div class="navigation">
        <h1 class="navigation-header">PORTFOLIO</h1>
        <hamburger-menu class="hamburger-menu" @some-event="callback"/>   
    </div>
    



    <img 
    class="profile-image" 
    :src="require('@/assets/profilbild_enrico_carruba2.png')" 
    alt="Enrico Carruba">
   
    <h1>Hello, my name is <br> <span> Enrico Carruba</span></h1>
    <p>I am a passionate junior <span> Web and Software Developer.</span></p>
    <p class="welcome-text">Welcome to my digital CV and portfolio page! Feel free to contact me.</p>
</template>
<script>
import hamburgerMenu from "./hamburgerMenu.vue";

export default {
    components: {
        hamburgerMenu,
    },
    methods: {
        callback(){
            console.log("emit funktioniert");
        }
    }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Sora:wght@100;200;300;400;500;600;700;800&display=swap');

.navigation{
    color: darkslategray;
    font-size: 1rem;
    text-align: left;
    display: flex;
    justify-content: space-between;
    background-color: white;
    position: fixed;
    width: 100%;
   
}

.hamburger-menu{
    display: flex;
    align-items: center;
    margin-right: 1rem;
}

.navigation-header{
    margin-left: 1rem;
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

