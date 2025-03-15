<script setup>
let person = {
    name:"Tamim Iqbal",
    age:"38",
    address:"Chattagram",
    phone:"017639567777"
}
</script>

<template>
    <h1>Person Info</h1>
    <h2>Name: {{ person.name }}</h2>
    <h2>Name: {{ person.age }}</h2>
    <h2>Name: {{ person.phone }}</h2>
    <h2>Name: {{ person.address }}</h2>
    
</template>

<style scoped>
h1{
    color:red;
}
h2{
    color:rgb(11, 131, 51);
}

</style>
