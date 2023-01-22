<template>
        <header>
            <div class="stars">
                <img src="@/assets/star.png" alt="star" id="star" class="one"> 
                <img src="@/assets/star.png" alt="star" id="star" class="two"> 
                <img src="@/assets/star.png" alt="star" id="star" class="three"> 
                <img src="@/assets/star.png" alt="star" id="star" class="four"> 
            </div>
        </header>
        <div class="comming">
            <div class="name">
                <h1>Alexandre Quemeneur</h1>      
                <h2>Frontend developer</h2>
                <h3>Vue.js</h3>
            </div>
            <div class="planet">
                <img src="@/assets/terre.png" alt="hearth" class="hearth" >     
            </div>           
        </div>   
</template>

<script>
import {gsap} from "gsap";
    export default {
        name: "HeaderComponent",

        mounted(){
            gsap.fromTo(".one",{y:600}, {
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
//BASES
header{
    background-color: rgb(30, 30, 28);
    #star{
        width: 50px;
    }
    .stars{
    display: flex;
    justify-content: space-around;
    .one{
    transform: rotate(45deg);
    }
    .two{
        transform: rotate(24deg);
    }
    .three{
        transform: rotate(13deg);
    }
}
}
.comming{
    background-color: rgb(30, 30, 28);
}
h1{
    font-family: "oleragie";
}



//MOBILE
@media screen and (max-width: 425px){
    .comming{
        display: flex;
        flex-direction: column;
        padding: 20px;
        h1{
            font-size: 10px;
        }
        h2{
            margin-left: 5px;
        }
        h3{
            margin-left: 10px;
        }
        .hearth{
            width: 200px;
            
        }
        .planet{
           align-self: flex-end; 
        }
    }

}



//TABLETTE
@media screen and (min-width:426px) and (max-width: 1180px){
    .comming{
        display: flex;
        justify-content: center;
        align-items: center;
        h1{
            font-size: 20px;
        }
        h2{
            margin-left: 5px;
        }
        h3{
            margin-left: 15px;
        }
        .hearth{
            width: 400px;
        }
    }
}


//ORDI
@media screen and (min-width:1181px){
    .comming{
        display: flex;
        justify-content: center;
        align-items: center;
        h1{
            font-size: 35px;
        }
        .name{
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        .hearth{
            margin-bottom: -135px;
            width: 750px;
        }
    }

}
</style>