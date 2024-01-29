<script setup>
    import cars from '../data/cars.json'
    import { RouterLink } from "vue-router"
</script>

<template>
   <h1>Home View</h1>
   <ul class="cars">
    <router-link  :to="`/cars/${car.Strain}`" v-for="car in cars" :key="car.id"><li>{{ car.Strain }}</li></router-link>
   </ul>
</template>

<style scoped>
    /* .cars {
        display: flex;
    }
    .cars a {
        text-decoration: none;
        color: white;   
        width: 100%;
        box-shadow: 1px 1px 1px whitesmoke;
    } */
</style>