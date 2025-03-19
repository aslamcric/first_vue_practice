
<script setup>
import axios from 'axios';
import { onMounted, ref } from 'vue';
  let month= ref("RAMADAN")
  let show= ref(true);

    let products=[
     {id:1, name:"Potato"},
     {id:2, name:"Apple"},
     {id:3, name:"Mango"},
     {id:4, name:"Lichi"},
     {id:5, name:"Lemon"},
   ]


   let customersLaravel= ref([])
   onMounted(()=>{
      axios.get("http://localhost/Laravel/Laravel_POS/public/api/find_customer")
      .then(res =>{
         console.log(res);
         customersLaravel.value=res.data.customer; 
      }).catch(err =>{
        console.log(err)
      })
       
   });
</script>


<template>
    <div class="container mt-4">
        <hr>

        <!-- Show/Hide Section -->
        <div class="text-center mt-3">
            <h1 v-if="show" class="fw-bold">This is {{ month }}</h1>
            <button @click="show = !show" class="btn btn-primary mt-2">Show/Hide</button>
        </div>

        <!-- Fruit List -->
        <div class="col-md-8 mx-auto mt-4">
            <h2 class="fw-semibold text-center">Fruit List</h2>
            <ul class="list-group mt-2">
                <li class="list-group-item" v-for="product in products" :key="product.id">
                    {{ product.name }}
                </li>
            </ul>
        </div>

        <hr>

        <!-- Customer Table -->
        <div class="table-responsive mt-4">
            <h2 class="fw-semibold text-center pb-3">Table Binding from Laravel API Customers</h2>
            <table class="table table-striped table-bordered table-hover">
                <thead class="table-dark">
                    <tr>
                        <th class="text-center fw-semibold">ID</th>
                        <th class="text-center fw-semibold">Name</th>
                        <th class="text-center fw-semibold">Phone</th>
                        <th class="text-center fw-semibold">Email</th>
                        <th class="text-center fw-semibold">Address</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="customer in customersLaravel" :key="customer.id">
                        <td class="text-center">{{ customer.id }}</td>
                        <td>{{ customer.name }}</td>   
                        <td>{{ customer.phone }}</td>   
                        <td>{{ customer.email }}</td>   
                        <td>{{ customer.address }}</td>   
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>






<style  scoped>

</style>