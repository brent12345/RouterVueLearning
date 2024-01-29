<script setup>
    import {useRoute} from "vue-router"
    import cars from "../data/cars.json"

    const route = useRoute()
    const car = cars.find(c => c.Strain.toLowerCase() === route.params.id.toLowerCase())

</script>


<template>
    <div v-if="car">
        <h1>
            New information
        </h1>
        <p>{{ car.update.adding }}</p>
        <p>{{ car.update.newdata }}</p>
        </div>
    <div v-else>
        No cars here!!
    </div>
</template>