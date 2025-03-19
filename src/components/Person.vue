<script setup>
let person = {
    name:"Tamim Iqbal",
    age:"38",
    address:"Chattagram",
    phone:"017639567777"
}
</script>

<template>
    <div class="container mt-4">
        <h1 class="text-center mb-4">Personal Info</h1>

        <div class="person-info">
            <div class="row mb-3">
                <div class="col-3 fw-bold">Name:</div>
                <div class="col">{{ person.name }}</div>
            </div>

            <div class="row mb-3">
                <div class="col-3 fw-bold">Age:</div>
                <div class="col">{{ person.age }}</div>
            </div>

            <div class="row mb-3">
                <div class="col-3 fw-bold">Phone:</div>
                <div class="col">{{ person.phone }}</div>
            </div>

            <div class="row mb-3">
                <div class="col-3 fw-bold">Address:</div>
                <div class="col">{{ person.address }}</div>
            </div>
        </div>
    </div>
</template>


<style scoped>
h1{
    color:red;
}
h2{
    color:rgb(11, 131, 51);
}

</style>
