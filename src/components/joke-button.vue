<template>
  <div>
    <h1 id="api">{{ joke }}</h1>
    <button @click="loudJoke" id="loud-button">Normal Joke</button>
    <button id="snake-button">Snake Button</button>
    <button id="normal-button">Loud Button</button>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            joke: "Normal Joke"
        }
    },
  methods: {
    loudJoke: function() {
      axios
        .request({
          url: "https://geek-jokes.sameerkumar.website/api?format=json",
          method: "GET"
        })
        .then(response => {
          this.joke = response.data.joke;
        })
        .catch(error => {
          console.log(error);
        });
    }
  }
};
</script>

<style scoped>
</style>