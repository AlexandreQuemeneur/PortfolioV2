<template>
        <header>
        <div class="stars">
            <img src="@/assets/star.png" alt="" id="star" class="on"> 
            <img src="@/assets/star.png" alt="" id="star" class="two"> 
            <img src="@/assets/star.png" alt="" id="star" class="three"> 
            <img src="@/assets/star.png" alt="" id="star" class="four"> 
        </div>
      
        <h1>Alexandre Quemeneur</h1>      
        <h2>Développeur web Frontend</h2>
    </header>
</template>

<script>
import {gsap} from "gsap";
    export default {
        name: "HeaderComponent",

        mounted(){
            gsap.fromTo(".on",{y:600}, {
                y:150,
                duration: 5.2,
                yoyo: true,
                repeat: 1000,
            });
            gsap.fromTo(".two",{}, {
                y:169,
                duration: 4,
                yoyo: true,
                repeat: 1000,
            });
             gsap.fromTo(".three",{}, {
                y:100,
                duration: 5,
                yoyo: true,
                repeat: 1000,
            });
            gsap.fromTo(".four",{}, {
                y:240,
                duration: 4.5,
                yoyo: true,
                repeat: 1000,
            });
        },
    }

</script>





<style lang="scss" scoped>


header{
    width: 100%;
    height: 100vh;
    background-color: rgb(30, 30, 28);
    #star{
        width: 50px;
    }
}
h1{
    font-family: "oleragie";
}
.stars{
    display: flex;
    justify-content: space-around;
}
@media screen and (max-width: 320px){
    h1{
        font-size: 20px;
    }
}
</style>