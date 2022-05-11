<template>
    <div class="my-cv-container">
        <h3>My CV</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea totam iusto saepe, ab blanditiis voluptatibus corporis vel voluptas! Alias iste doloremque aliquam placeat nemo modi? Ipsum sapiente mollitia neque omnis?</p>
        <button 
        id="btn-container" @click="showSections = !showSections, toggleBtnText($event)">More details</button>
        <transition>
                <div class="sections" v-show="showSections">
                    <section id="section1">
                        <article>
                            <h3>{{  experiences[0].title    }}</h3>
                            <p> {{  experiences[0].content  }} </p>
                            <button id="btn-article1" @click="expandArticle1 = !expandSection1, toggleBtnText($event)">More details</button>
                        </article>
                        <article>
                            <h3>{{  experiences[1].title    }}</h3>
                            <p> {{  experiences[1].content  }} </p>
                            <button id="btn-article2" @click="expandArticle2 = !expandSection1, toggleBtnText($event)">More details</button>
                        </article>
                        <article>
                            <h3>{{  experiences[2].title    }}</h3>
                            <p> {{  experiences[2].content  }} </p>
                            <button id="btn-article3" @click="expandArticle3 = !expandSection1, toggleBtnText($event)">More details</button>
                        </article>
                        
            
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
            expandArticle1: false,
            expandArticle2: false,
            expandArticle3: false,
            btnText: "More details",
            
            experiences: experiences,
        }
    },
    methods: {
        toggleBtnText(event){
            let button = document.getElementById(event.target.id);   
            if(button.innerHTML == "More details"){
                button.innerHTML = "Less details";
            } else {
                button.innerHTML = "More details";
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