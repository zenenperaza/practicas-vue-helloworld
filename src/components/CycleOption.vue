<template>
<div> 
    hola mundo !!
</div>
</template>

<script lang="ts" setup>
import { onMounted, onUpdated } from 'vue';

onMounted(() => {
    console.log("onMounted");
})

onUpdated(() => {
    console.log("onUpdated");
})



//    OPTIOM API
// export default defineComponent({
//     name: "CycleOption",
//     created(){
//         console.log("created")   
//     },
//     mounted() {
//       console.log("mounted")
//     },
//     updated() {
//        console.log("updated") 
//        },
//     unmounted() {
//         console.log("unmounted")
//     },
// })
</script>

<style scoped>

</style>