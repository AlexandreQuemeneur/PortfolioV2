<template>
    <section id="skills">  
        <div class="about">
            <div class="planet">
                <img src="@/assets/saturne.png" alt="saturne" class="saturne" >
            </div>  
            <div class="myself">      
                <p>I am a beginner front-end developer who recently graduated from the O'clock web and mobile developer school. I have a good knowledge of Vue.js and have had the opportunity to put my skills into practice by creating projects using this technology. I also master HTML, CSS, and JavaScript and have a good understanding of web development best practices. I am passionate about learning new technologies.</p>
            </div>
        </div>

        <div class="boxglass">
            <h4>My tools</h4>
            <div class="boxone">
                <img src="@/assets/logo/icon-vuejs.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-javascript.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-gsap.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-sass.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-npm.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-git.svg" alt="" class="glass">
            </div>
            <div class="boxtwo">
                <img src="@/assets/logo/icon-html.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-css.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-axios.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-api.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-jwt.svg" alt="" class="glass">
                <img src="@/assets/logo/icon-wp.svg" alt="" class="glass">
            </div>
        </div>       
    </section>
</template>

<script>
export default {
    name: "SkillsComponent",
}
</script>

<style lang="scss" scoped>

//SKILLS
#skills{
    margin: none;
    background-color: rgb(30, 30, 28);
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

//MOBILE
@media screen and (max-width: 425px){
    #skills{
        display: flex;
        flex-direction: column;
    }
    .saturne{
        width: 200px;
    }
    .about{
        display: flex;
        justify-content: space-around;
        flex-direction: column;
        .myself{
            padding: 5px;
            margin: 20px 10px;
        }
    }
    .boxglass{
    margin: none;
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
    h4{
        margin-top: 30px;
    }
    .glass{    
        padding: 7px 0;
        white-space: nowrap;
        width: 10%;
    } 
    .boxone{
        margin: none;
        display: flex;
        justify-content: flex-end;
        border-top: 1px solid rgb(57, 55, 55);
        img{
            margin: auto;
        }
    }
    .boxtwo{
        margin: none;
        display: flex;
        justify-content: flex-end;
        border-bottom: 1px solid rgb(57, 55, 55);
        margin-bottom: 50px;
        img{
            margin: auto;
        }
    }
}
}
//TABLETTE
@media screen and (min-width: 426px) and (max-width: 1180px){
    .boxglass{
    margin: none;
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
    h4{
        margin-top: 70px;
    }
    .glass{    
        padding: 7px 0;
        white-space: nowrap;
        width: 10%;
    } 
    .boxone{
        margin: none;
        display: flex;
        justify-content: flex-end;
        border-top: 1px solid rgb(57, 55, 55);
        img{
            margin: auto;
        }
    }
    .boxtwo{
        margin: none;
        display: flex;
        justify-content: flex-end;
        border-bottom: 1px solid rgb(57, 55, 55);
        margin-bottom: 50px;
        img{
            margin: auto;
        }
    }
}
.saturne{
    width: 350px;
}
}
//ORDI
@media screen and (min-width:1181px){
    #skills{
        background-color: rgb(30, 30, 28);
        display: flex;
        justify-content: center;
        align-items: center;
        p{
            margin: 5% 7%;
            padding: 20px;
            font-size: 25px;
        }
    }
    .about{
        display: flex;
        .myself{
            display: flex;
            justify-content: center;
            align-items: center;
            
        }
    }

    .planet{
        margin-bottom: 40px;
        .saturne{
            width: 650px;
        }
    }
    .boxglass{
        margin-bottom: 220px;
    }
    .boxglass{
    margin: none;
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
    margin-bottom: 50px;
    .glass{    
        padding: 7px 0;
        white-space: nowrap;
        width: 5%;
    } 
    .boxone{
        margin: none;
        display: flex;
        justify-content: flex-end;
        margin-top: 10px;
        border-top: 1px solid rgb(57, 55, 55);
        img{
            margin: auto;
        }
    }
    .boxtwo{
        margin: none;
        display: flex;
        justify-content: flex-end;
        border-bottom: 1px solid rgb(57, 55, 55);
        margin-bottom: 50px;
        img{
            margin: auto;
        }
    }
}
}
</style>