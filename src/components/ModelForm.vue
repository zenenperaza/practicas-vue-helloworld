<template>
    <h1 >{{ inputText }} </h1>
<form action="">
    <input type="text" v-model="inputText" /><br>
    <input type="checkbox" v-model="agree"> Acepto los terminos <br>
    <select name="" id="">
        <option value="Spain">Spain</option>
        <option value="UK">UK</option>
        <option value="Portugal">Portugal</option>
    </select>
</form>
    </template>
    
    <script lang="ts" setup>

        import { ref } from "vue";

        let inputText = ref('')
        let agree = ref(true)
        let country = ('UK')       
        

    </script>
    
    <style scop>
    
    </style>