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
            <h1 class = "h1-text">{{ $t('welcome') }}</h1>
            <p class = "text">
                {{ $t('homeText') }}
            </p>
            <div class="btn-container">
                <Btn :text="$t('resume')" @click = "openCV()"/>
                <Btn :text="$t('contact')" href="#contact"/>
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
    margin: auto 0;
}
.image img{
    height: 300px;
    width: 350px;
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
@media screen and (max-width: 1400px) {
  #home {
    height: 83vh;
    margin-bottom: 6rem;
  }
}
@media screen and (max-width: 1200px) {
  #home {
    display: block;
  }
  .text{
    width:fit-content
  }
  .image img {
    width: 300px;
    height: 275px;
    margin: 0 auto 2rem;
  }

}
@media screen and (max-width: 600px) {
    #home {
      height: 83vh;
      margin-bottom: 0;
    }
    .container{
        padding: 2rem;
    }
}
</style>
