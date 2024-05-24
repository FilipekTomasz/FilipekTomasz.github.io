<script setup lang="ts">
defineProps<{
  text: string
  link: string
}>()
</script>

<template>
    <a :href="link">{{ text }}</a>
</template>

<style scoped>
    a{
      color: var(--lightgrey);
      transition: color 0.5s;
      padding: 0 20px;
      text-decoration: none;
    }
    a:hover{
      color: var(--darkgrey);
    }
</style>