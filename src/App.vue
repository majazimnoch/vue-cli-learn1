<template>
  <img alt="Vue logo" src="./assets/goldie.webp">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <h2>{{ 2 + 3 + 5 }}</h2>
  <h2>Add method - {{ add(10,15,20) }}</h2>
  <h2>Multiply method - {{ multiply(baseValue) }}</h2>
  <div>
    <button v-on:click="changeName($event), increment(1, $event)">Change name
    </button>
  </div>
  <div>
    <h2>{{name}}</h2>
    <div>
      <button v-on:click="name = 'Maja'">Change Button</button>
      <button v-on:mouseover="changeName">Hover Button</button>
    </div>
    <div>
      <h2>{{ count }}</h2>
      <button v-on:click="increment(2)">Increment by 2</button>
      <button v-on:click="count -=1">Decrement by 1</button>
    </div>
  </div>
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
      baseValue: 2,
      name: 'Marta',
      count: 0
    }
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply (num) {
      return num * this.baseMultiplier
    },
    increment(num) {
      this.count += num
    },
    changeName(event) {
this.name = 'batman'
console.log('Event', event)
    }
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
