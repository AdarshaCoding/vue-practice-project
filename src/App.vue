<template>
  <Home />
</template>

<script>
import HomePage from "./HomePage.vue"
  export default {
    name: "App",
    components:{
      "Home":HomePage    //HomePage - then render with <HomePage /> instead of just <Home />
    }  
  }
</script>

<style scoped>
  
</style>
