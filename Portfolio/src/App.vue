<script setup>
import { RouterLink, RouterView } from "vue-router";
import HeaderComponent from "@/components/HeaderComponent.vue";
import SkillsComponent from "@/components/SkillsComponent.vue";
import ProjectComponent from "@/components/ProjectComponent.vue";
import ContactComponent from "@/components/ContactComponent.vue";
</script>

<template>
    <div ref="counter" v-if="loading">
        <div  class="loader">
            <p>{{ counter }}</p>           
        </div>  
    </div>

    <div  v-else>
        <headerComponent />
        <SkillsComponent />
        <ProjectComponent />  
        <ContactComponent /> 
    </div>
    
     
</template>


<script>
import gsap from "gsap";
    export default {
        name: app,
        data() {
        return {
            loading: true,
            counter: 0,
        }
    },
    mounted() {
        let intervalId = setInterval(() => {
            if (this.counter === 100){               
                clearInterval(intervalId) 
                setTimeout(() => {
                gsap.to(this.$refs.counter, { 
                    opacity: 0,
                    duration: 1,
                    ease: "elastic.inOut",
                });     
                setTimeout(() => {          
                this.loading = false
            }, 500)
        }, 500)
            } else {
                this.counter++
            }          
        }, 20)

        let docTitle = document.title;
        window.addEventListener('blur', () => {
        document.title = "Come Back 🥹";
        });
        window.addEventListener('focus', () => {
        document.title = docTitle;
        });
    },
}
    
</script>

<style lang="scss" >
*{
  margin: 0;
  padding: 0;
  color: white;
  box-sizing: border-box;
}
@font-face {
    font-family: "morely";
    src: url(@/assets/fonts/GishellaMorely.ttf);
}
@font-face {
    font-family: "oleragie";
    src: url(@/assets/fonts/OleragiePersonalUse-axj1g.ttf);
}
h4{
    font-family: "oleragie";
}
.loader{
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgb(30, 30, 28); 
    height: 100vh;
}
//MOBILE
@media screen and (max-width: 425px){
    .loader{
        p{
            font-size: 100px;
            color: rgb(255, 255, 255);
            font-family: "morely";
        }
    }
}

//TABLETTE
@media screen and (min-width:426px) and (max-width: 1180px){
    .loader{
        p{
            font-size: 150px;
            color: rgb(255, 255, 255);
            font-family: "morely";
        }
    }
}

//DESKTOP
@media screen and (min-width: 1181px){
    .loader{
        p{
            font-size: 200px;
            color: rgb(255, 255, 255);
            font-family: "morely";
        }      
    }
}
</style>
