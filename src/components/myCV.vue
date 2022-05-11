<template>
    <div class="my-cv-container">
        <h3>My CV</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea totam iusto saepe, ab blanditiis voluptatibus corporis vel voluptas! Alias iste doloremque aliquam placeat nemo modi? Ipsum sapiente mollitia neque omnis?</p>
        <button @click="showSections = !showSections; toggleBtnText()"> {{ btnText }}</button>
        <transition>
                <div class="sections" v-show="showSections">
                    <section>
                        <h3>{{  experiences[0].title    }}</h3>
                        <p> {{  experiences[0].content  }} </p>
                        <button @click="expandSection1 = !expandSection1; toggleBtnText(button)"> {{ btnText }}</button>
                        
                        
                        <!-- <div v-for="experience in experiences" :key="experience.id"> 
                            <h3>{{experience.title}}</h3>  
                            <p>{{experience.content}}</p> 
                            <button @click="showSections = !showSections; toggleBtnText()"> {{ btnText }}</button>
                        </div> -->

                    </section>
                </div>
        </transition>
    </div>

</template>

<script>
import experiences from "./experience.json";

export default {
    components: {
        
    },
    data() {
        return {
            showSections: false,
            expandSection1: false,

            btnText: "More details",
            
            experiences: experiences,
        }
    },
    methods: {
        toggleBtnText(button){
            if(button.value == "More details"){
                this.btnText = "Less details";
            } else {
                this.btnText = "More details";
            }
        },
    }
}
</script>

<style>

.my-cv-container {
    width: 90vw;
    height: 100%;
    margin: 1rem;
    box-shadow: 0px 0px 25px lightgrey;
}

h3 {
    margin: 1rem;
    padding-top: 1rem;
    color: gray;
}
</style>