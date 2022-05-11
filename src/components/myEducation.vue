<template>
    <div class="my-edu-container">
        <h3>My Education</h3>
        <p>Here you can find my past vocational education and my university degree.</p>
        <button id="btn-container" @click="showDetails = !showDetails, toggleBtnText($event)">More details</button>
            <transition>
                <article v-show="showDetails">
                    <div class="table-container">
                        <p>2018 - 2019</p> 
                        <p id="position"> Friseur</p>   
                        <p>THE BARBERSHOP Hannover</p>
                    </div>
                    <div class="table-container">
                        <p>2011 - 2017</p> 
                        <p id="position"> B.A. Economics & Business Psychology</p>   
                        <p>University of Applied Sciences Euro-FH Hamburg</p>
                    </div>
                    <div class="table-container">
                        <p>2002 - 2004</p> 
                        <p id="position"> Kaufmann im Groß- und Außenhandel</p>   
                        <p>Georg Kugelmann GmbH</p>
                    </div>
                    <hr>
                </article>
            </transition>
    </div>
</template>

<script>
export default {
    data(){
        return {
            showDetails: false,
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

.my-edu-container {
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

.table-container p{
    font-weight: 300;
    margin: 0.5rem 1rem 0.5rem 1rem;
}

#position {
    font-weight: bolder;
}

</style>