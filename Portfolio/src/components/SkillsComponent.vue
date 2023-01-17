<template>
    <section id="skills">  
        <div class="about">
            <div class="planet">
                <img src="@/assets/saturne.png" alt="saturne" class="saturne" >
            </div>  
            <div class="myself">      
                <p>Je suis un développeur front-end débutant ayant récemment obtenu mon diplôme de développeur web et web mobile avec l'école O'clock. J'ai une bonne connaissance de Vue.js et j'ai eu l'occasion de mettre en pratique mes compétences en créant des projets en utilisant cette technologie. Je maîtrise également HTML, CSS et JavaScript, et j'ai une bonne compréhension des bonnes pratiques de développement web. Je suis passionné par l'apprentissage de nouvelles technologies.</p>
            </div>
        </div>

        <div class="boxglass">
            <img src="@/assets/logo/icon-vuejs.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-javascript.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-sass.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-npm.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-git.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-html.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-css.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-axios.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-ajax.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-api.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-jwt.svg" alt="" class="glass">
            <img src="@/assets/logo/icon-wp.svg" alt="" class="glass">
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
.glass{    
    padding: 7px 0;
    white-space: nowrap;
    width: 5%;
}

.boxglass{
    overflow: hidden;
    margin: none;
    display: flex;
    justify-content: flex-end;
    border-bottom: 1px solid rgb(57, 55, 55);
    border-top: 1px solid rgb(57, 55, 55);
    margin-bottom: 50px;
    img{
        margin: auto;
    }
}
@media screen and (max-width: 414px){
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
    }
}
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
        .saturne{
            width: 700px;
        }
    }
}
</style>