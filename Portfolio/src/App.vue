<script setup>
import { RouterLink, RouterView } from "vue-router";
import HeaderComponent from "@/components/HeaderComponent.vue";
import SkillsComponent from "@/components/SkillsComponent.vue";
import ProjectComponent from "@/components/ProjectComponent.vue";
import ContactComponent from "@/components/ContactComponent.vue";
import LoaderComponent from "@/components/LoaderComponent.vue";
</script>

<template>
    <div v-if="loading">
       <LoaderComponent />
    </div>

    <div v-else>
        <headerComponent />
        <SkillsComponent />
        <ProjectComponent />  
        <ContactComponent /> 
    </div>
    
     
</template>


<script>
    export default {
        name: app,
        data(){
            return {
                loading: true,
            }
        },
        mounted() {
            setTimeout(() => {
            this.loading = false
            }, 5000)
        }
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
</style>
