<template>
    <section id="projects">
        <h2>All my projects :</h2>
        <section class="project ecolomind">
            <h3>Ecolomind</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo, quisquam?</p>
            <a href=""><img src="@/assets/lien.png" alt="link to ecolomind"></a>
            <div class="tech">
                
            </div>
        </section>
        <section class="project portfolio">
            <h3>Portfolio</h3>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rerum, ducimus.</p>
            <a href=""><img src="@/assets/lien.png" alt="link to portfolio"></a>
            <div class="tech">

            </div>
        </section>
        <section class="project vintage">
            <h3>Vintage shop</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, fugiat!</p>
            <a href=""><img src="@/assets/lien.png" alt="link to Vintage shop"></a>
            <div class="tech">

            </div>
        </section>
        <section class="project wlm">
            <h3>We love movie</h3>
            <h4>comming soon</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, fugiat!</p>
            <a href=""><img src="@/assets/lien.png" alt="link to Vintage shop"></a>
            <div class="tech">

            </div>
        </section>
    </section>
</template>

<script>
export default {
    name: "ProjectComponent",
}
</script>

<style lang="scss" scoped>

//PROJECTS
#projects{
    width: 100%;
    height: 100vh;
    background-color: rgb(30, 30, 28);
}
h2{
    margin-bottom: 20px;
}
.project{
    border-bottom: 1px solid white; 
}
.ecolomind{
    border-top: 1px solid white;
}
@media screen and (max-width: 415px){
    .project{
        width: 70%;
        height: 20%;
        padding: 5px 0;
        margin-left: 5%; 
        h3{
            margin-bottom: 20px;
        }    
        img{
            width: 30px;
        }        
    }
}
@media screen and (min-width:416px) and (max-width: 1180px){
    .project{
        width: 80%;
        height: 20%;
        padding: 5px 0;
        margin-left: 5%; 
        h3{
            margin-bottom: 20px;
        }    
        img{
            width: 30px;
        }        
    }
}
@media screen and (min-width:1181px){
    .project{
        width: 80%;
        height: 20%;
        padding: 5px 0;
        margin-left: 5%; 
        h3{
            margin-bottom: 20px;
        }    
        img{
            width: 30px;
        }        
    }
}
</style>