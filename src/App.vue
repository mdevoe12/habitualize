<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <Welcome :name="username"/>

  <input type="checkbox" v-model="workout"/>
  <label>Workout</label>
  <button @click="clearData">Clear Data</button>
</template>

<script>
import Welcome from './components/Welcome.vue'

export default {
  data() {
    return {
      username: 'Matt',
      workout: false
    }
  },
  name: 'App',
  components: {
    Welcome
  },
  methods: {
    clearData() {
      this.workout=false
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
