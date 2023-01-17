<template>
        <header>
        <div class="stars">
            <img src="@/assets/star.png" alt="star" id="star" class="on"> 
            <img src="@/assets/star.png" alt="star" id="star" class="two"> 
            <img src="@/assets/star.png" alt="star" id="star" class="three"> 
            <img src="@/assets/star.png" alt="star" id="star" class="four"> 
        </div>
        <div class="comming">
            <div class="name">
                <h1>Alexandre Quemeneur</h1>      
                <h2>Développeur web Frontend</h2>
            </div>
            <div class="planet">
                <img src="@/assets/terre.png" alt="hearth" class="hearth" >
            </div>
        </div>
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

@media screen and (max-width: 376px){
   header{
    h1{
        font-size: 10px;
    }

    .planet{
        display: flex;
        justify-content: space-around;
        img{
        width: 120px;
        height: 120px;
        }
    }
}
}
@media screen and (min-width:377px) and (max-width: 1180px){
    header{
    h1{
        font-size: 20px;
    }
    img{
        width: 50px;
    }
    .planet{
        display: flex;
        justify-content: space-around;
    }
}
}
@media screen and (min-width:1181px){
    header{
    h1{
        font-size: 35px;
    }
    .planet{
        display: flex;
        justify-content: space-around;
        img{
        width: 750px;
        .hearth{
            align-self: flex-start;
        }
        }
    }
    .name{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin: 80px 0 0 50px;
        align-self: flex-start;
    }
    .comming{
        display: flex;
    }
}
}
</style>