<template>
    <div class="portfolio-component-container">
        <h3>My portfolio</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea totam iusto saepe, ab blanditiis voluptatibus corporis vel voluptas! Alias iste doloremque aliquam placeat nemo modi? Ipsum sapiente mollitia neque omnis?</p>
        <button @click="showProjects = !showProjects; toggleBtnText()"> {{ btnText }}</button>
            <transition>
            <div class="first-section" v-show="showProjects">
                <section>
                   <p v-if="reposLoaded"> {{ this.repos[0] }} </p>
                </section>
            </div>
             
            </transition>
           

    </div>
</template>

<script>
export default {
    created() {
         fetch('https://api.github.com/users/enricocarruba/repos')
        .then(resp => resp.json())
        .then(data => this.repos = data)
        .catch(err => console.log(err.message))
    },
    
    data() {
        return {
            showProjects: false,
            btnText: "Show details",
            repos: [],
        }
    },
    methods: {
        toggleBtnText(){
            if(this.btnText == "More details"){
                this.btnText = "Less details";
            } else {
                this.btnText = "More details";
            }
        }
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
</style>