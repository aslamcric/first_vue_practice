<script setup>
import { ref } from 'vue';
let count= ref(0);
const increase =()=> count.value ++;
const decrease =()=> count.value --;
</script>

<template>
    <div class="container mt-4">
        <hr>
        <h1 class="text-center">Counter App</h1>

        <h2 class="text-center">Value: {{ count }}</h2>

        <div class="d-flex justify-content-center gap-3 mt-4">
            <button @click="decrease" class="btn btn-danger">Minus</button>
            <button @click="increase" class="btn btn-success">Plus</button>
        </div>
    </div>
</template>

<style scoped>
h1{
    color: red;
}
</style>