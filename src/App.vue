<template>
  <div id="app">
    <CounterGroup></CounterGroup>
  </div>
</template>

<script>
import CounterGroup from "./components/CounterGroup";

export default {
  name: 'App',
  components: {
    CounterGroup
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
