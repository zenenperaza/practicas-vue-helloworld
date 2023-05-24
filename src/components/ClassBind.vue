<template>
    <div v-bind:style="{backgroundColor : '#ccc', color: color}">
        El mensaje fue enviado
 
 </div>
 <button @click="handleClick">Cambia Color</button>
</template>

<script lang="ts" >
import { defineComponent, ref } from "vue";
export default defineComponent({
    name: 'ClassBind',
    setup(){
        let color = ref('#fff')
        const handleClick = () => {color.value = "#ff0000" }
        return {color, handleClick}
    }
})
    
</script>

<style>

</style>