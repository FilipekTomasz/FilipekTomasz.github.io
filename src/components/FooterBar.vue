<script setup lang="ts">
    import NavLink from './NavLink.vue';
</script>
<template>
    <nav class="desktopNav">
        <ul class ="tabs">
            <li><NavLink text="Home" link="#home" /></li>
            <li><NavLink text="Projects" link="#projects" /></li>
            <li><NavLink text="Contact" link="#contact" /></li>
        </ul>
    </nav>
    <!--<p>Copyright &#169; 2024 Tomasz Filipek. All Rights Reserved.</p>-->
</template>
<style scoped>
    ul{
    padding: 0;
    }

    .desktopNav{
        align-items: center;
        display: flex;
        justify-content: center;
        top: 0;
        width: 100vw;
        height: 26vh;
        z-index: 99;
    }
    .tabs{
        align-items: center;
        display: flex;
        justify-content: flex-end;
        list-style: none;
    }

    p {
        text-align: center;
    }
    @media screen and (max-width: 600px) {
        li, .tabs{
            font-size: 1.5rem;
        }
    }
</style>