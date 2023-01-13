<template>
    <div class="loader">
        <h1>{{ counter }}</h1>
    </div>
</template>

<script>
export default {
    name: 'LoaderComponent',
    data() {
        return {
            loading: true,
            counter: 0,
        }
    },
    mounted() {
        let intervalId = setInterval(() => {
            if (this.counter === 100){
                clearInterval(intervalId)
                this.loading = false
            } else {
                this.counter++
            }          
        }, 50)
    }
}
</script>

<style lang="scss" scoped>

h1{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    font-size: 200px;
    color: rgb(255, 255, 255);
    font-family: "morely";
}
.loader {
    background-color: rgb(30, 30, 28);    
}
</style>