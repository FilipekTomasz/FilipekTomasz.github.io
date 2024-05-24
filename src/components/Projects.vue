<script setup lang="ts">
import Btn from './Btn.vue';
function openSite(link:string){
    window.open(`${link}`, '_blank');
}
</script>
<template>
    <section id="projects">
        <p class="text_1">Browse my</p>
        <h2 class="text_2">Projects</h2>
        <div class="projects-container">
          <div class="project-container color-container">
            <div class="img-container">
              <img
                src="../assets/wsp.png"
                alt="wsp"
                class="project-img"
              />
            </div>
            <div class="project-text-container">
              <h2 class="project-title">WSP</h2>
              <p class="project-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, 
                  quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            </div>
            <div class="btn-container">
                <Btn text="Github" @click="openSite('https://github.com/FilipekTomasz/wsp-backend')"/>
                <Btn text="Live" @click="openSite('https://wsp.zs6sobieski.edu.pl/')"/> 
            </div>
          </div>

          <div class="project-container color-container">
            <div class="img-container">
              <img
                src="../assets/wsp.png"
                alt="wsp"
                class="project-img"
              />
            </div>
            <div class="project-text-container">
              <h2 class="project-title">Project Two</h2>
              <p class="project-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, 
                  quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu 
                  fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>
            </div>
            <div class="btn-container">
                <Btn text="Github"/>
                <Btn text="Live"/>
            </div>
          </div>

          <div class="project-container color-container">
            <div class="img-container">
              <img
                src="../assets/wsp.png"
                alt="wsp"
                class="project-img"
              />
            </div>
            <div class="project-text-container">
              <h2 class="project-title">Project Three</h2>
              <p class="project-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, 
                  quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            </div>
            <div class="btn-container">
                <Btn text="Github"/>
                <Btn text="Live"/>
            </div>
          </div>

        </div>
        <div class="btn-more-container">
            <Btn text="Show more"  @click="openSite('https://github.com/FilipekTomasz?tab=repositories')"/>
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
.project-img {
  border-radius: 2rem;
  width: 400px;
  height: 400px;
  border: black 0.1rem solid;
}
.project-title {
  margin: 1rem;
  color: black;
}
.project-text {
  text-align: center;
  margin: 0;
  width: 400px;
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
    flex-direction: column;
    align-items: center;
  }
}

@media screen and (max-width: 768px) {
  .text_2 {
    font-size: 2rem;
  }
}

</style>