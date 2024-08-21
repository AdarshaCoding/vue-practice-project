<template>
  <div class="body">
    <div class="section-one">
      <div class="data-container">
        <h2 :style="{ textAlign: 'center' }">{{ this.count }}</h2>
      </div>
      <div class="operations">
        <!-- <button class="std-btn" v-on:click="this.count++">Increment</button> -->
        <!-- <button class="std-btn" v-on:click="this.count--">Decrement</button> -->
        <button class="std-btn" @click="increment">Increment</button>
        <button class="std-btn" v-on:click="decrement">Decrement</button>
      </div>
      <hr />
      <div class="data-entry">
        <!--
            v-bind:style or :style
        -->
        <label :style="{ color: 'Orange', fontSize: 20 + 'px' }">Search</label>
        <input type="text" v-model="searchText" placeholder="Search" />
        <span :style="{ paddingLeft: 10 + 'px' }">{{ searchText.length }}</span>
      </div>
      <hr />
      <div class="loops-section">
        <h4>Ordered Items</h4>
        <ul class="items">
          <li v-for="item in items">{{ item }}</li>
        </ul>
      </div>
    </div>
    <div class="test-component">
      <TestComponent />
    </div>
  </div>
</template>

<script>
import TestComponent from './TestComponent.vue'

export default {
  name: 'Body',
  components: { TestComponent },
  data: function () {
    return {
      //state variables and default values
      count: 0,
      searchText: '',
      items: ['Apple', 'Banana', 'Grapes', 'Orange'],
      user: [
        { name: 'Adarsha', city: 'Bengaluru', country: 'India' },
        { name: 'Deepa', city: 'Mandya', country: 'India' },
        { name: 'Darsha', city: 'Mysore', country: 'India' }
      ]
    }
  },
  created: function () {
    console.log('1st Life cycle method: Created')
  },
  mounted: function () {
    console.log('2nd Life cycle method: Mounted')
    return this.count++
  },
  methods: {
    increment() {
      return this.count++
    },
    decrement() {
      if (this.count > 0) {
        return this.count--
      }
    }
  }
}
</script>

<style scoped>
.section-one {
  border: 1px solid white;
  padding: 20px;
}

.test-component {
  border: 1px solid white;
  padding: 20px;
  width: 280px;
}
.body {
  background-color: rgb(55, 45, 56);
  color: white;
  min-height: 90vh;
  padding: 10px;
  display: flex;
  justify-content: space-evenly;
}

.std-btn {
  padding: 5px;
  border-radius: 5px;
  cursor: pointer;
}

.operations {
  padding-bottom: 10px;
  text-align: center;
}

.data-entry {
  padding-top: 10px;
  padding-bottom: 10px;
}

input {
  margin-left: 5px;
  padding: 5px;
  outline-style: none;
}

.loops-section {
  padding-top: 10px;
  padding-bottom: 10px;
}

.items {
  padding-left: 30px;
}
</style>
