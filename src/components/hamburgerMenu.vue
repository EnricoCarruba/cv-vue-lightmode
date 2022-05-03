<template>
    <div class="hamburger-container" @click="toggle(); $emit("someEvent")">
        <div class="hamburg">
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return {
            toggled: false,
        }
    },
    methods: {
        toggle(){
            this.toggled = !this.toggled;
            var hamburger = document.querySelector(".hamburg");
            hamburger.onclick = function () {
            this.classList.toggle ("checked");
            }
        },
        secondFun(){
            console.log("läuft");
        }
    }
}
</script>

<style>

.hamburg { 
   display: block;
   background: #555; width: 75px; height: 50px; 
   position: relative; 
   margin-left: auto; margin-right: auto;
   border-radius: 4px; 
   transition: border-radius .5s;
}

.line { 
   position: absolute; 
   left:10px;
   height: 4px; width: 55px; 
   background: #fff; border-radius: 2px;
   display: block; 
   transition: 0.5s; 
   transform-origin: center; 
}

.line:nth-child(1) { top: 12px; }
.line:nth-child(2) { top: 24px; }
.line:nth-child(3) { top: 36px; }

.hamburg.checked .line:nth-child(1){
   transform: translateY(12px) rotate(-45deg);
}

.hamburg.checked .line:nth-child(2){
   opacity:0;
}

.hamburg.checked .line:nth-child(3){
   transform: translateY(-12px) rotate(45deg);
}

</style>