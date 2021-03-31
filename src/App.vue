<template>
  <clock></clock>
</template>

<script>
import Clock from './components/Clock'

export default {
  name: 'App',
  components: {
    Clock
  }
}
</script>

<style lang="scss">
body {
  background-color: #12141C;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
