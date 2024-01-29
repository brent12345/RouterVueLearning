<script setup>
import { useRoute, useRouter, RouterView } from 'vue-router'
import cars from '../data/cars.json'
import ContactView from './ContactView.vue'

const route = useRoute()
console.log(route.params)
const router = useRouter()
console.log(router)

const strainName = route.params.id

const car = cars.find(c => c.Strain === strainName)
console.log(cars)

console.log(route.params.id)

const showContact = () => {
    if (strainName != '13-Dawgs') {
        router.push(`/cars/${strainName}/contact`)
    }
}
</script>

<template>
    <div v-if="car">
    
        <h1>{{ car.Strain }}</h1>
    
        <p>{{ car.Rating }}</p>
    
        <p>{{ car.Type }}</p>
    
        <p>{{ car.Flavor }}</p>
    
        <p>{{ car.Effects }}</p>
    
        <p>{{ car.Description }}</p>
    
        <button @click="showContact">Click for more information</button>
    
        <RouterView />
    
    </div>
    <div v-else>Car not found</div>
</template>

<style>

</style>