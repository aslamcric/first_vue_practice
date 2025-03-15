<script setup>
import { ref } from 'vue';
let count= ref(0);
const increase =()=> count.value ++;
const decrease =()=> count.value --;
</script>

<template>
    <hr>
    <h1>Counter App</h1>

    <h2>Value: {{ count }}</h2>
    <!-- <button @click="count++">++</button>
    <button @click="count--">--</button> -->


    <button @click="increase">++</button>
    <button @click="decrease">--</button>

</template>

<style scoped>
h1{
    color: red;
}
</style>