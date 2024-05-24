<script setup lang="ts">
defineProps<{
  text: string
}>()
</script>
<template>
    <button>{{ text }}</button>
</template>
<style scoped>
  button{
    font-weight: 600;
    padding: 0.7rem;
    width: 9.5rem;
    border-radius: 2rem;
    transition: all 300ms ease;
    border: rgb(53, 53, 53) 0.1rem solid;
    cursor: pointer; 
    background: rgb(53, 53, 53);
    color: white;
}
button:hover{
  background: rgb(20,20,20);
  border: rgb(255, 255, 255) 0.1rem solid;
}

</style>