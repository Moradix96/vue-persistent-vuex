<template>
  <div id="app">
    <div>Counter:</div>
    <div>{{ $store.state.count }}</div>
    <button @click="onIncrease">+</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  methods: {
    onIncrease(){
      this.$store.commit('increase');
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
