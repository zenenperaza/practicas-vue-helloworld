<template>
<h1 v-show="age < 18"  >Es menor de edad</h1>
<h1 v-show="age >= 18"  >Es mayor de edad</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
    name: 'ExampleOptionAPI',
    setup(){
        let age = 18
        return {age}
    }
})
   
</script>

<style scop>

</style>



<!-- COMPOSITION API
<script lang="ts" setup>
    let age = 10
</script> -->