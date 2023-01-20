<template>
    <section id="projects">
        <h4>All my projects :</h4>
        <section class="project ecolomind">
            <h3>Ecolomind</h3>
            <p>In a context where ecology is starting to take a prominent place in the collective consciousness, people may not know where to begin this transition.
            This website would be a platform where everyone could share their tips on how to act in this direction. Project: Allow users to submit and consult ideas, tips.</p>
            <a target="_blank" href="https://ecolomind.tk/#/"><img src="@/assets/lien.png" alt="link to ecolomind"></a>
            <div class="tech">
                
            </div>
        </section>
        <section class="project portfolio">
            <h3>Portfolio</h3>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rerum, ducimus.</p>
            <a target="_blank" href="https://alexandre-quemeneur.fr/"><img src="@/assets/lien.png" alt="link to portfolio"></a>
            <div class="tech">

            </div>
        </section>
        <section class="project vintage">
            <h3>Vintage shop</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, fugiat!</p>
            <a target="_blank" href=""><img src="@/assets/lien.png" alt="link to Vintage shop"></a>
            <div class="tech">

            </div>
        </section>
        <section class="project wlm">
            <h3>We love movie</h3>
            <p>comming soon</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, fugiat!</p>
            <a href=""><img src="@/assets/lien.png" alt="link to Vintage shop"></a>
            <div target="_blank" class="tech">

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
@media screen and (max-width: 415px){
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
    }
    #projects{
    width: 100%;
    background-color: rgb(30, 30, 28);
}
}
@media screen and (min-width:416px) and (max-width: 1180px){
    .project{
        width: 80%;
        // height: 30%;
        padding: 5px 0;
        margin-left: 5%; 
        h3{
            margin-bottom: 20px;
        }    
        img{
            width: 30px;
        }        
    }
    #projects{
    width: 100%;
    background-color: rgb(30, 30, 28);
}
}
@media screen and (min-width:1181px){
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
    }
    #projects{
    width: 100%;
    background-color: rgb(30, 30, 28);
}
}
</style>