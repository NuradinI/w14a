<template>
  <div id="app">
<joke-button/>
  </div>
</template>

<script> 
import JokeButton from './components/joke-button.vue';

export default {
  name: "App",
  components: {
  JokeButton
  }
};
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
