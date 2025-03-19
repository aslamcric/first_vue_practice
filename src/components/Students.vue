<template>
    <div class="container">
    
    <hr>
    <h1>Student List</h1>

    <ol v-html="students">
        
    </ol>
</div >
    
</template>

<script lang="ts" setup>
let students = `
    <li>Razib</li>
    <li>Salman</li>
    <li>Aslam</li>
    <li>Sowrov</li>
    <li>Shawon</li>
`

</script>

<style>

</style>