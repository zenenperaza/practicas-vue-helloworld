<template>
<h1 v-show="age < 18">Es menor de edad</h1>
<h1 v-show="age > 18">Es mayor de edad</h1>
</template>

<script lang="ts" setup>
    let age = 10
</script>

<style scop>

</style>