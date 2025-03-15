<template>
    <hr>
    <h1 v-show="toggle">{{ headline }}</h1>

    <button @click="toggle = !toggle">Show/Hide</button>


    <p :id="paragraph_id">Lorem ipsum dolor sit, amet consectetur adipisicing elit. In, provident expedita temporibus magni ratione commodi ut eos. Quam vitae ex modi consectetur reiciendis dicta minus velit, ducimus fuga asperiores labore aliquam neque voluptate, minima mollitia quisquam praesentium consequatur eaque officiis eos veritatis dolorum, doloremque architecto. Atque numquam nostrum incidunt delectus.</p>
    <br>

    <!-- <input v-model="headline" type="text" placeholder="headline"> -->

    
    <button @click="changId()">change Id</button>
    <!-- <button @click="changId" >change Id</button> -->
</template>

<script lang="ts" setup>
import { ref } from 'vue';

let headline = ref("IsDB-BISEW");

let toggle = ref(true);

let paragraph_id = ref("asset");

const changId = () => {
   paragraph_id.value = paragraph_id.value === "asset" ? "paragraph" : "asset"; 
};
</script>

<style>
#asset {
    color: rgb(255, 0, 64);
}
#paragraph {
    color: rgb(0, 85, 33);
}
</style>
