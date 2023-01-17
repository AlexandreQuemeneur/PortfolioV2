<template>
    <section id="skills">
        <div class="blabla">
            
                <h2>Skills</h2>
                <p>Je suis un développeur front-end débutant ayant récemment obtenu mon diplôme de développeur web et web mobile avec l'école O'clock. J'ai une bonne connaissance de Vue.js et j'ai eu l'occasion de mettre en pratique mes compétences en créant des projets en utilisant cette technologie. Je maîtrise également HTML, CSS et JavaScript, et j'ai une bonne compréhension des bonnes pratiques de développement web. Je suis passionné par l'apprentissage de nouvelles technologies.</p>

        </div>

        <div class="boxglass">
            <div class="glass">
                <p>HTML 5</p>
            </div>
            <div class="glass">
                <p>CSS / SASS</p>
            </div>
            <div class="glass">
                <p>JavaScript</p>
            </div>
            <div class="glass">
                <p>Vue.js</p>
            </div>
            <div class="glass">
                <p>Gsap</p>
            </div>
            <div class="glass">
                <p>Php</p>
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
    width: 100%;
    padding: 15px;
    background-color: rgb(30, 30, 28);
    display: flex;
    justify-content: center;
    align-items: center;
}
.glass{    
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 15px;
    width: 200px;
    height: 50px;
    background: rgba(255, 255, 255, 0.15);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.3);
}
.boxglass{
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

}
.blabla{
    width: 50%
}
@media screen and (max-width: 414px){
    #skills{
        display: flex;
        flex-direction: column;
    }
}
@media screen and (min-width:1181px){
    #skills{
    width: 100%;
    height: 100vh;
    padding: 15px;
    background-color: rgb(30, 30, 28);
    display: flex;
    justify-content: center;
    align-items: center;
}
}
</style>