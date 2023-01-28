<template>
    <section id="projects">
        <h4 id="trigger">All my projects :</h4>
        <section class="project ecolomind">
            <h3>Ecolomind</h3> 
            <div class="link">
                <p>In a context where ecology is starting to take a prominent place in the collective consciousness, people may not know where to begin this transition.
                This website would be a platform where everyone could share their tips on how to act in this direction. Project: Allow users to submit and consult ideas, tips.</p>  
                <a target="_blank" href="https://ecolomind.tk/#/"><img src="@/assets/lien.png" alt="link to ecolomind"></a>     
            </div>      
            <div class="tech">
                <img src="@/assets/logo/icon-vuejs.svg" alt="logo vue.js">
                <img src="@/assets/logo/icon-javascript.svg" alt="logo javascript">
                <img src="@/assets/logo/icon-gsap.svg" alt="logo gsap">
                <img src="@/assets/logo/icon-sass.svg" alt="logo sass">
                <img src="@/assets/logo/icon-wp.svg" alt="logo wordpress">
                <img src="@/assets/logo/icon-axios.svg" alt="logo axios">               
            </div>
        </section>

        <section class="project portfolio">
            <h3>Portfolio</h3>
            <div class="link">
                <p>This portfolio was created with Vue.js and allowed me to learn how to use the GSAP library.</p>
            </div>
            
            <div class="tech">
                <img src="@/assets/logo/icon-vuejs.svg" alt="logo vue.js">
                <img src="@/assets/logo/icon-javascript.svg" alt="javascript">
                <img src="@/assets/logo/icon-gsap.svg" alt="logo gsap">
                <img src="@/assets/logo/icon-sass.svg" alt="logo sass">
            </div>
        </section>

        <section class="project vintage">
            <h3>Vintage shop</h3>
            <div class="link">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, fugiat! Lorem ipsum dolor sit amet consectetur adipisicing elit. </p>
                <a target="_blank" href=""><img src="@/assets/lien.png" alt="link to Vintage shop"></a>  
            </div>         
            <div class="tech">
            </div>
        </section>

        <section class="project wlm">
            <h3>We love movie</h3>
            <p class="commings">comming soon</p>
            <div class="link">
                <p>A movie library creation website, with rating system. Tools for randomly selecting movies and more.</p>
                <!-- <a target="_blank" href=""><img src="@/assets/lien.png" alt="link to Vintage shop"></a> -->
            </div>
            <div class="tech">
            </div>
        </section>
    </section>
</template>

<script>
import gsap from 'gsap';
export default {
    name: "ProjectComponent",
    mounted(){
        let tl = gsap.timeline({
            scrollTrigger: {
                trigger: "#trigger",
                start: "top",
            }
        });
        tl.fromTo(".ecolomind", {opacity: 0, x: -100, y: 100 }, {opacity: 1, duration:1, x: 0, y: 0 })
        .fromTo(".portfolio", {opacity: 0, x: -100, y: 100 }, {opacity: 1, duration:1, x: 0, y: 0 })
        .fromTo(".wlm", {opacity: 0, x: -100, y: 100 }, {opacity: 1, duration:1, x: 0, y: 0 })
    }
}
</script>

<style lang="scss" scoped>

h4{
    margin-bottom: 20px;
}
.project{
    border-bottom: 1px solid white; 
}
.ecolomind{
    border-top: 1px solid white;
}
.vintage{
    display: none;
}
.tech{
    display: flex;
    justify-content: flex-start;
    align-content: flex-start;
    margin: auto;
    img{
        margin: auto 5px;
    }
}
//MOBILE
@media screen and (max-width: 425px){
    .project{
        width: 70%;
        padding: 5px 0;
        margin-left: 5%; 
        h3{
            margin-bottom: 20px;
        }   
        img{
            width: 30px;
        }   
        p{
            padding-right: 20px;
        }     
    }
    #projects{
    width: 100%;
    background-color: rgb(30, 30, 28);
    h4{
        margin-left:10px;
    } 
}
}

//TABLETTE
@media screen and (min-width:426px) and (max-width: 1180px){
    .project{
        width: 80%;
        padding: 5px 0;
        margin-left: 5%; 
        h3{
            margin-bottom: 20px;
        }  
        img{
            width: 30px;
        }
        p{
            padding-right: 150px;
        }        
    }
    #projects{
    width: 100%;
    background-color: rgb(30, 30, 28);
    h4{
        margin-left:30px;
    }  
}
}
@media screen and (min-width:1181px){
    .project{
        width: 80%;
        padding: 5px 0;
        margin-left: 5%; 
        h3{
            font-size: 40px;
            margin: 20px 0;
        }    

        img{
            width: 35px;
        }
        p{
            font-size: 20px;
            padding-right: 450px;
        }  
        .commings{
                font-size: 35px;  
                margin-bottom: 20px;     
            }
        .link{
            display: flex;
            a{
                margin-right: 15px;
            }
            p{
                margin-bottom: 15px;
            }
            
        }      
    }
    #projects{
    width: 100%;
    background-color: rgb(30, 30, 28);
    h4{
        margin-left: 50px;
    }
}
}
</style>