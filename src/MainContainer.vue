<template>
  <div class="body">
    <div class="data-container">
      <h2>{{ this.count }}</h2>
    </div>
    <div class="operations">
      <!-- <button class="std-btn" v-on:click="this.count++">Increment</button> -->
      <!-- <button class="std-btn" v-on:click="this.count--">Decrement</button> -->
      <button class="std-btn" @click="increment">Increment</button>
      <button class="std-btn" v-on:click="decrement">Decrement</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Body',
  data: function () {
    return {
      count: 0
    }
  },
  mounted: function () {
    console.log('Body: Component is mounted!')
    return this.count++
  },
  methods: {
    increment() {
      return this.count++
    },
    decrement() {
      return this.count--
    }
  }
}
</script>

<style scoped>
.body {
  background-color: rgb(55, 45, 56);
  color: white;
  min-height: 90vh;
  padding: 10px;
}

.std-btn {
  padding: 5px;
  border-radius: 5px;
  cursor: pointer;
}
</style>
