<template>
    <div :class="{'danger' : hasError}">
        El mensaje fue enviado
 
 </div>
</template>

<script lang="ts" >
import { defineComponent } from "vue";
export default defineComponent({
    name: 'ClassBind',
    data(){
        return {
            hasError: true
        }
    }
})
 

</script>

<style>
.danger {
    color: red;
}
</style>