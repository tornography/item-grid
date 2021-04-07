<template>
  <div id="app">
    <Example />
  </div>
</template>

<script>
import Example from './components/Example.vue';

export default {
  name: 'App',
  components: {
    Example,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
