<template>
    <h1 >{{ inputText }} </h1>
<form action="">
    <input type="text" v-model="inputText" />
</form>
    </template>
    
    <script lang="ts" setup>

    import { Ref, ref } from "vue";

    let inputText:Ref<string> = ref('')
    </script>
    
    <style scop>
    
    </style>