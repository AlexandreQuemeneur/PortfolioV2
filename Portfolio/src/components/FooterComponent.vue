<template>
        <footer>
        
        <div><p class="boop">&#169;2023 Alexandre quemeneur, All Rights Reserved </p></div>
        <div class="social">
           <a target="_blank" href="https://github.com/AlexandreQuemeneur"><img src="@/assets/github.png" alt="github-logo"></a> 
           <a target="_blank" href="https://www.linkedin.com/in/alexandre-quemeneur/"><img src="@/assets/linkedin.png" alt="linkedin-logo"></a> 
           <a target="_blank" href="https://twitter.com/Octave_DeLaBath"><img src="@/assets/twitter.png" alt="twitter-logo"></a>
        </div>

       
    </footer>
</template>

<script>
export default {
    name: "FooterComponent",
}
</script>

<style lang="scss" scoped>

footer{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgb(30, 30, 28);
    max-height: 500px;
}
.social{
    width:50%;
    display: flex;
    justify-content: flex-end;
    align-items: center;

    img{
        width: 30px;
        height: 30px;
        margin: 0 10px 2px 10px;
    }
}

</style>