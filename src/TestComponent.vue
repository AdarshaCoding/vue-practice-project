<template>
  <div class="test-parent">
    <h3>Test Component</h3>
    <hr />
    <button
      v-on:click="checkEligibility"
      v-bind:style="{
        marginRight: 10 + 'px',
        marginTop: 5 + 'px',
        backgroundColor: 'lightBlue',
        padding: 2 + 'px',
        borderRadius: 5 + 'px'
      }"
    >
      Toggle
    </button>
    <span>{{ this.eligible }}</span>
  </div>
</template>
<script>
export default {
  name: 'TestComponent',
  data: function () {
    return {
      firstName: 'Adarsha',
      lastName: 'PC',
      city: 'Bangalore',
      eligible: true
    }
  },
  created() {
    console.log(this.firstName)
    console.log(this.$data)
  },
  methods: {
    checkEligibility() {
      this.eligible = !this.eligible
    }
  }
}
//https://medium.com/swlh/vue-js-understanding-data-methods-computed-and-watch-aa97df7d979a
</script>
<style></style>
