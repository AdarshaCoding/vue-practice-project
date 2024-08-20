<template>
  <header>
    <h1>Hello World!</h1>
    <h1>{{ msg }}</h1>
  </header>
</template>

<script>
  export default{
    name: "App"
    data: function () {
      return {
        msg:"Hello World!"
      }
    }
  }
</script>


<style scoped>

</style>
