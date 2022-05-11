<template>
    <div class="my-cv-container">
        <h3>My CV</h3>
        <p>I do not have that tipical straight CV as you will see. To easily get an overview you will find three categories with its detail information.</p>
        <button id="btn-container" @click="showSections = !showSections, toggleBtnText($event)">More details</button>
        <transition>
                <div class="sections" v-show="showSections">
                    <section id="section1">
                        <article>
                            <h3>{{      experiences[0].title    }}</h3>
                            <span> {{   experiences[0].year   }}</span>
                            <p> {{      experiences[0].content  }} </p>
                            <button id="btn-article1" @click="expandArticle1 = !expandArticle1, toggleBtnText($event)">More details</button>
                                <div class="table-container" v-show="expandArticle1" v-for="experience in experiences[0].experiences" :key="experience.id">
                                        <p >{{ experience.year }}</p> 
                                        <p id="position"> {{  experience.position }}</p>   
                                        <p> {{  experience.company }}</p>
                                </div>
                            <hr>
                        </article>
                        <article>
                            <h3>{{      experiences[1].title    }}</h3>
                            <span> {{   experiences[1].year   }}</span>
                            <p> {{      experiences[1].content  }} </p>
                            <button id="btn-article2" @click="expandArticle2 = !expandArticle2, toggleBtnText($event)">More details</button>
                                <div class="table-container" v-show="expandArticle2" v-for="experience in experiences[1].experiences" :key="experience.id">
                                        <p >{{ experience.year }}</p> 
                                        <p id="position"> {{  experience.position }}</p>   
                                        <p> {{  experience.company }}</p>
                                </div>
                            <hr>
                        </article>
                        <article>
                            <h3>{{      experiences[2].title    }}</h3>
                            <span> {{   experiences[2].year   }}</span>
                            <p> {{      experiences[2].content  }} </p>
                            <button id="btn-article3" @click="expandArticle3 = !expandArticle3, toggleBtnText($event)">More details</button>
                                <div class="table-container" v-show="expandArticle3" v-for="experience in experiences[2].experiences" :key="experience.id">
                                        <p >{{ experience.year }}</p> 
                                        <p id="position"> {{  experience.position }}</p>   
                                        <p> {{  experience.company }}</p>
                                </div>
                            <hr>
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

article h3{
    color: black;
    margin: 0 0 0 1rem;
}

article span {
    margin: 0 0 1rem 1rem;
    font-size: 0.75rem;
}

.table-container{
    border: 1px solid lightblue;
}

.table-container p{
    font-weight: 300;
    margin: 0.5rem 1rem 0.5rem 1rem;
}

#position {
    font-weight: bolder;
}

</style>