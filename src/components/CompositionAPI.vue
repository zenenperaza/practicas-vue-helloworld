<template>
<div> 
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
</div>
</template>

<script lang="ts" setup>
import { ref, Ref } from "vue";
let counter:Ref = ref(0)
const addCounter = ():void => {
    counter.value++
}
        
</script>

<style scoped>

</style>            