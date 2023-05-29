<template>
<div> 
    <label for="" v-custom-font.sm.blue>Subtotal</label>
    <input type="numer" v-model="subtotal">
    <h3 v-custom-font.xl.red>Total impuestos a pagar: {{ totalIVA }} ({{ iva }})%</h3>
</div>
</template>

<script lang="ts" setup>
    import { Ref, ref, computed } from "vue";

    const iva = 21
    let subtotal:Ref<number> = ref(0)
    const totalIVA = computed(() => (iva*subtotal.value / 100))

   
</script>

<style scoped>

</style>