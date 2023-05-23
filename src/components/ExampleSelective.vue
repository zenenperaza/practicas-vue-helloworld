<template>
<h1 v-if="age < 18">Es menor de edad</h1>
<h1 v-else>Es mayor de edad</h1>
</template>

<script lang="ts" >
import { defineComponent } from 'vue';
export default defineComponent({
    name:'ExampleSelective',
    setup(){
        let age = 10
        return {age}
    }
})
</script>

<style scoped>

</style>