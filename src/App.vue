<template>
  <img alt="Vue logo" src="./assets/logo.png">
</template>

<script>
import { createApp } from 'vue'
import Container from './components/Container'

export default {
  name: 'App',
  mounted() {
    window.createPPT = this.createPPT
  },
  methods: {
    createPPT(options) {
      createApp(Container, {options}).mount('body')
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
