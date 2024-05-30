<script setup lang="ts">
import Btn from './Btn.vue';
function openSite(link:string){
    window.open(`${link}`, '_blank');
}
</script>
<template>
    <section id="projects">
        <p class="text_1">{{ $t('browse') }}</p>
        <h2 class="text_2">{{ $t('projects') }}</h2>
        <div class="projects-container">
          <div class="project-container color-container">
            <div class="img-container">
              <img
                src="../assets/wsp1.png"
                alt="wsp"
                class="project-img"
              />
            </div>
            <div class="project-text-container">
              <h2 class="project-title">WSP</h2>
              <p class="project-text">{{ $t('projectsText1') }}</p>
            </div>
            <div class="btn-container">
                <Btn text="Github" @click="openSite('https://github.com/FilipekTomasz/wsp-backend')"/>
                <Btn :text="$t('live')" @click="openSite('https://wsp.zs6sobieski.edu.pl/')"/> 
            </div>
          </div>

          <div class="project-container color-container">
            <div class="img-container">
              <img
                src="../assets/wyprowadz1.png"
                alt="wsp"
                class="project-img"
              />
            </div>
            <div class="project-text-container">
              <h2 class="project-title">Wyprowadz mnie</h2>
              <p class="project-text">{{ $t('projectsText2') }}</p>
            </div>
            <div class="btn-container">
                <Btn text="Github" @click="openSite('https://github.com/FilipekTomasz/wyprowadzmnie')"/>
                <Btn :text="$t('live')"/>
            </div>
          </div>

          <div class="project-container color-container">
            <div class="img-container">
              <img
                src="../assets/olympus3.png"
                alt="wsp"
                class="project-img"
              />
            </div>
            <div class="project-text-container">
              <h2 class="project-title">Olympus</h2>
              <p class="project-text">{{ $t('projectsText3') }}</p>
            </div>
            <div class="btn-container">
                <Btn text="Github" @click="openSite('https://github.com/EverestAPI/Olympus/pull/89')"/>
                <Btn :text="$t('live')" @click="openSite('https://everestapi.github.io/')"/>
            </div>
          </div>

        </div>
        <div class="btn-more-container">
            <Btn :text="$t('showMore')"  @click="openSite('https://github.com/FilipekTomasz?tab=repositories')"/>
        </div>

    </section>
</template>
<style scoped>

#projects{
  position: relative;
  height:auto;
}
.projects-container {
  display: flex;
  justify-content: center;
  gap: 1rem;
}
.btn-container {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top:1rem;
}

.text_1 {
  text-align: center;
  margin: 0;
}

.text_2 {
  font-size: 3rem;
  text-align: center;
}

.img-container {
  display: flex;
  text-align: initial;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-around;
}
.project-container {
  display: flex;
  flex-direction: column;
  padding: 1.5rem;
  background: white;
  border-radius: 2rem;
  border: rgb(53, 53, 53) 0.1rem solid;
  border-color: rgb(163, 163, 163);
  text-align: center;
  width: fit-content;
}
.color-container {
  border-color: rgb(163, 163, 163);
  background: rgb(250, 250, 250);
}
.img-container img{
  border-radius: 1rem;
  max-width: 400px;
  max-height: 220px;
  border: black 0.1rem solid;
}
.project-title {
  margin: 1rem;
  color: black;
}
.project-text {
  text-align: center;
  margin: 0;
}
.project-text-container {
    flex-grow: 1;
}
.btn-more-container{
    margin: 1rem auto;
    width:fit-content;
}

@media screen and (max-width: 1400px) {
  section {
    margin: 0 2rem;
  }

  .projects-container {
    flex-wrap: wrap;
  }
  #projects{
    height: fit-content;
  }
}
@media screen and (max-width: 1200px) {
  .projects-container{
    margin-top: 2rem;
    padding:0.5rem;
  }
  .img-container img{
    width: 275px;
  }
  #projects{
    margin-top:100px;
  }


}
</style>