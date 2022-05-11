<template>
    <div class="navigation">
        <h1 class="navigation-header">PORTFOLIO & CV</h1>
       <!--  <hamburger-menu class="hamburger-menu" @click-event="toggleNavigationList()"/>   
            <div class="navigation-list" v-show="isToggledHeaderNavigation">
                <ul>
                    <li>
                        <img id="download-img" :src="require('@/assets/download.svg')" alt="">
                        <a @click="download()">Download CV</a>
                    </li>
                    <li>
                        <img class="navigation-logos" :src="require('@/assets/GitHub_Logo.png')" alt="">
                        <a href="https://github.com/EnricoCarruba">My Github profile</a>
                    </li>
                    <li>
                        <a @click="download()">Contact me</a>
                    </li>
                </ul>
            </div> -->
    </div>

    <div class="header-text-container">
        <div class="header-text">
            <h1>Hello,</h1>
            <p>my name is Enrico Carruba.</p>
            <p>I am a passionate junior <br> <span> Web and Software Developer </span> <br> from Hannover.</p>
            <p class="welcome-text">Welcome to my digital CV and Portfolio page! Feel free to contact me.</p>
        </div>
        
    </div>
    <div class="profile-image-container" >
                <img id="profile-image"
                :src="require('@/assets/profilbild_enrico_carruba.png')" 
                alt="Enrico Carruba"/>
    </div>
   
</template>
<script>
// import hamburgerMenu from "./hamburgerMenu.vue";

export default {
    data() {
        return {
            isToggledHeaderNavigation: false,
        }
    },
    components: {
        // hamburgerMenu,
    },
    methods: {
        toggleNavigationList(){
            this.isToggledHeaderNavigation = !this.isToggledHeaderNavigation;
        },
        download(){
            window.open("https://github.com/EnricoCarruba/cv-vue-lightmode/raw/main/src/assets/CV%20Enrico%20Carruba%20.pdf");
        }
    },

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
    display: inline-flexbox;
    top: 0;
    width: 100%;
    box-shadow: 10px 0 25px lightgrey;
}

.hamburger-menu{
    display: flex;
    align-items: center;
    margin-right: 1rem;
}

.navigation-header{
    margin-left: 1rem;
    
}

.navigation-list{
    background-color: lightgrey;
    position: absolute;
    top: 5rem;
    width: 100%;
}

.navigation-logos{
    height: 10vh;
    width: 10vw;
}

li {
    list-style: none;
}

.navigation-list-items{
    list-style-type: none;
}

.download-img {
    height: 150px;
    width: 150px;
}

.header-text-container{
    width: 90vw;
    height: 45vh;
    margin: 6.5rem 1rem 0rem 1rem;
    box-shadow: 0px 0px 25px lightgrey;
}

.header-text-container h1{
    color: salmon;
    margin-left: 1rem;
}

.header-text {
    margin: 0;
    padding-top: 0.05rem;
}

.header-text span {
    font-weight: bolder;
}

.profile-image-container{
    width: 90vw;   
    height: 50vh;
    margin: 0 1rem 0 1rem;
}

#profile-image{
    width: 100%;
    height: 100%;
    object-fit: cover;
}



</style>

