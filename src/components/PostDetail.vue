<template>
<div class="post"> 
    <h3>{{ props.title }}</h3>
    <p>{{ props.content }}</p>
    <input type="text" v-model="message"/>
    <button @click="handleClick">Di Hola</button>

</div>
</template>

<script lang="ts">
import { defineComponent, Ref, ref } from "vue";
export default defineComponent({
    name: 'PostDetail',
    props: {
        title:{
            type: String,
            required: true
        },
        content : {
            type: String,
            requiered: false,
            default: "Post sin contenido"
        }
    },
    emits: ["sayHi"],
    setup(props, {emit}){
        let message:Ref<string> = ref("")
        const handleClick = () => {
           emit("sayHi", message.value)
        }
        return {props, message, handleClick}
    }
})
   
</script>

<style scoped>
.post{
    width: 300px;
    height: 200px;
    border-radius: 10px;
    background-color: antiquewhite;
    margin: 10px;
    padding: 10px;


}
</style>