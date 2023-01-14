<template>
    <section id="skills">
        <div class="blabla">
            
                <h2>Skills</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum beatae quod quaerat, suscipit cumque aspernatur saepe asperiores eveniet, rerum placeat, architecto quis facere est repudiandae perferendis id doloremque perspiciatis voluptatem cupiditate error odio! Maiores sed similique debitis illum temporibus autem omnis rerum cupiditate voluptate maxime?</p>

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
    // height: 100vh;
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
@media screen and (max-width: 375px){
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