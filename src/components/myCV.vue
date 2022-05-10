<template>
    <div class="my-cv-container">
        <h3>My CV</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea totam iusto saepe, ab blanditiis voluptatibus corporis vel voluptas! Alias iste doloremque aliquam placeat nemo modi? Ipsum sapiente mollitia neque omnis?</p>
        <button @click="showSections = !showSections; toggleBtnText()"> {{ btnText }}</button>
        <transition>
                <div class="categories">
                    
                </div>
        </transition>
    </div>

</template>

<script>
export default {
    data() {
        return {
            showSections: false,
            btnText: "More details",
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