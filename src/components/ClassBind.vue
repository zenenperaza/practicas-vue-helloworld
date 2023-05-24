<template>
    <div v-bind:style="{backgroundColor : '#ccc', color: color}">
        El mensaje fue enviado
 
 </div>
 <button @click="handleClick">Cambia Color</button>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';

    let color = ref('#fff');
    
    const handleClick = () => color.value = '#ff0000'
    
</script>

<style>

</style>