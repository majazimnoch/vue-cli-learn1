<template>
  <img alt="Vue logo" src="./assets/goldie.webp">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <h2>{{ 2 + 3 + 5 }}</h2>
  <h2>Add method - {{ add(10,15,20) }}</h2>
  <h2>Multiply method - {{ multiply(baseValue) }}</h2>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      baseMultiplier: 5,
      baseValue: 2
    }
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply (num) {
      return num * this.baseMultiplier
    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

img {
width: 400px;
}
</style>
