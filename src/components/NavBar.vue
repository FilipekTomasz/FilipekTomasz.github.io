<script setup lang="ts">
import NavLink from './NavLink.vue';

function toggleHamburger(){
    const menu = document.querySelector(".menu-links");
    const icon = document.querySelector(".hamburger-icon");
    menu?.classList.toggle("open");
    icon?.classList.toggle("open");
}
</script>

<template>
    <nav class="desktopNav">
        <div class ="logo">Tomasz Filipek</div>
        <ul class ="tabs">
            <li><NavLink text="Home" link="#home" /></li>
            <li><NavLink text="Projects" link="#projects" /></li>
            <li><NavLink text="Skills" link="#skills" /></li>
            <li><NavLink text="Contact" link="#contact" /></li>
        </ul>
    </nav>
    <nav class="mobileNav">
        <div class ="logo">Tomasz Filipek</div>
        <div class ="hamburger-menu">
            <div class ="hamburger-icon" @click="toggleHamburger()">
                <span></span>
                <span></span>
                <span></span>
            </div>
            <div class="menu-links">
                <li><NavLink text="Home" link="#home" @click="toggleHamburger()"/></li>
                <li><NavLink text="Projects" link="#projects" @click="toggleHamburger()" /></li>
                <li><NavLink text="Skills" link="#skills" @click="toggleHamburger()" /></li>
                <li><NavLink text="Contact" link="#contact" @click="toggleHamburger()" /></li>
            </div>
        </div>
    </nav>
</template>

<style scoped> 
.desktopNav{
    align-items: center;
    display: flex;
    justify-content: space-evenly;
    position: fixed;
    top: 0;
    width: 100vw;
    z-index: 99;
}
.mobileNav{
    display:none;
    justify-content: space-around;
    align-items: center;
    height: 17vh;
}
.hamburger-menu{
    position:relative;
    display: inline-block
}
.hamburger-icon{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 24px;
    width: 30px;
    cursor: pointer;
}
.tabs{
    align-items: center;
    display: flex;
    justify-content: flex-end;
    list-style: none;
}

.hamburger-icon span {
    width:100%;
    height: 2px;
    background-color: black;
    transition: all 0.3 ease-in-out;
}
.menu-links{
    position: absolute;
    top: 100%;
    right: 0;
    background-color: white;
    width:fit-content;
    max-height: 0;
    overflow: hidden;
    transition: all 0.3 ease-in-out;

}

.hamburger-menu {
  position: relative;
  display: inline-block;
}

.hamburger-icon {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 24px;
  width: 30px;
  cursor: pointer;
}

.hamburger-icon span {
  width: 100%;
  height: 2px;
  background-color: black;
  transition: all 0.3 ease-in-out;
}

.menu-links {
  position: absolute;
  top: 100%;
  right: 0;
  background-color: white;
  width: fit-content;
  max-height: 0;
  overflow: hidden;
  transition: all 0.3 ease-in-out;
}

.menu-links a {
  display: block;
  padding: 10px;
  text-align: center;
  font-size: 1.5rem;
  color: black;
  text-decoration: none;
  transition: all 0.3 ease-in-out;
}

.menu-links li {
  list-style: none;
}

.menu-links.open {
  max-height: 300px;
}

.hamburger-icon.open span:first-child {
  transform: rotate(45deg) translate(10px, 5px);
}

.hamburger-icon.open span:nth-child(2) {
  opacity: 0;
}

.hamburger-icon.open span:last-child {
  transform: rotate(-45deg) translate(10px, -5px);
}

.hamburger-icon span:first-child {
  transform: none;
}

.hamburger-icon span:first-child {
  opacity: 1;
}

.hamburger-icon span:first-child {
  transform: none;
}


@media screen and (max-width:1200px){
    .desktopNav{
        display:none;
    }
    .mobileNav{
        display:flex;
    }
}

</style>
