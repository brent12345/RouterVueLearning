
<script setup>
    import {RouterLink} from "vue-router"
</script>


<template>
  <div>
    <router-link active-class="active" to="/">Home</router-link>  
    <router-link active-class="active" to="/about">Bout</router-link>  
  </div>
</template>

<style scoped>
    .active {
        font-weight: 900;
        color: gold;
    }
</style>
