<script setup lang="ts">
    import Btn from "./Btn.vue"
    function openCV(){
        window.open('src/assets/TomaszFilipekCV.pdf', "_blank")
    }
    function openSite(link:string){
        window.open(`${link}`, '_blank');
    }
</script>
<template>
    <section class="container" id="home">
        <div class ="info">
            <h1 class = "h1-text">Welcome!</h1>
            <p class = "text">
                My name is Tomasz Filipek and I'm a software engineer. 
                My passion is building web applications and designing websites using modern frameworks. 
                Also I love trying out new technologies.
            </p>
            <div class="btn-container">
                <Btn text="Open resume" @click = "openCV()"/>
                <Btn text="Contact" href="#contact"/>
            </div>
            <div class="socials-container">
                <img
                    src="../assets/linkedin.png"
                    alt="My LinkedIn profile"
                    class="icon"
                    @click="openSite('https://www.linkedin.com/in/tomasz-filipek-143360221/')"
                />
                <img
                    src="../assets/github.png"
                    alt="My Github profile"
                    class="icon"
                    @click="openSite('https://github.com/FilipekTomasz')"
                />
            </div>
        </div>
        <div class ="image">
            <img src="../assets/imgpc1.png" alt="Computer picture">
        </div>
       
    </section>
</template>
<style scoped>
.container{
    display:flex;
    justify-content: center;
    gap: 5rem;
    height: 80vh;
    width: 100vw;
}

.image{
    display:flex;
    height: 300px;
    width: 300px;
    margin: auto 0;
}
.info{
    align-self: center;
    text-align: center;

}
.btn-container{
    display:flex;
    justify-content: center;
    gap: 1rem;
}
.text{
    align-content: center;
    align-self: center;
    width:500px;
}
.socials-container {
  display: flex;
  justify-content: center;
  margin-top: 1rem;
  gap: 1rem;
}
.icon {
  cursor: pointer;
  height: 2rem;
}

</style>
