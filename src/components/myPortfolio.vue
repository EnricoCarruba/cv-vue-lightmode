<template>
    <div class="portfolio-component-container">
        <h3>My portfolio</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea totam iusto saepe, ab blanditiis voluptatibus corporis vel voluptas! Alias iste doloremque aliquam placeat nemo modi? Ipsum sapiente mollitia neque omnis?</p>
        <button @click="showProjects = !showProjects; toggleBtnText()"> {{ btnText }}</button>
            <transition>
            <div class="projects" v-show="showProjects">
                <section v-if="reposLoaded">
                   <h1>NAME</h1>
                   <h2>{{ this.repos[this.counter].name }} </h2>
                   <h1>DESCRIPTION</h1>
                   <p>{{ this.repos[this.counter].description }}</p>
                   <a :href="this.repos[this.counter].html_url">LINK to Github Repository</a>
                   <div class="repo-buttons">
                    <button @click="btnPrevious()">previous</button>
                    <button @click="btnNext()">next</button>
                   </div>
                </section>
            </div>
             
            </transition>

          
           

    </div>
</template>

<script>

export default {
    components: {
       
    },

    created() {
         fetch('https://api.github.com/users/enricocarruba/repos')
        .then(resp => resp.json())
        .then(data => this.repos = data)
        .catch(err => console.log(err.message))
    },
    
    data() {
        return {
            showProjects: false,
            btnText: "More details",
            repos: [],
            counter: 0,
        }
    },
    methods: {
        toggleBtnText(){
            if(this.btnText == "More details"){
                this.btnText = "Less details";
            } else {
                this.btnText = "More details";
            }
        },
        btnNext(){
            if(this.counter < this.repos.length){
                this.counter++; 
                }
            console.log(this.counter);
            console.log(this.repos.length);
        },
        btnPrevious(){
            if(this.counter >= 0){
            this.counter--; {
                if(this.counter == -1){
                    this.counter = 0;
                }
            }
            }
            console.log(this.counter);
            console.log(this.repos.length);
        },
    },
    computed: {
        reposLoaded(){
            return this.repos[0]?.name;
            
        }
    }
}
</script>

<style>
.portfolio-component-container {
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

p{
    margin: 1rem;
}

button {
    margin: 1rem;
}

.v-enter-active,
.v-leave-active {
  transition: opacity 0.7s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

.projects{
    width: 100%;
}

.projects h1 {
    color: lightgray;
    font-size: 1rem;
    margin: 1rem 0 0 1rem; 
}

.projects h2 {
    margin: 0 0 1rem 1rem;
}

.projects a {
    margin: 1rem;
}

.projects p {
    margin: 0 0 1rem 1rem;
}

.repo-buttons {
    
    display: flex;
    justify-content: center;
}

.repo-buttons button {
    width: 100px;
    height: 30px; 
    background-color: lightgrey;
    border: none;
    border-radius: 5px;
    font-weight: bolder;
}
</style>