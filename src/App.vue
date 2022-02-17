<template>
  <div id="app">
    <div>Counter:</div>
    <div>{{ $store.state.count }}</div>
    <div>Double: {{ doubleCounter }}</div>
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
  },
  computed: {
    doubleCounter: function () {
      return this.$store.state.count * 2
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
