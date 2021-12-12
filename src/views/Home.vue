<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <button v-on:click="stopIndex();"> Stop Feed </button>
    <p> {{ data }} </p>
  </div>
</template>

<style></style>

<script>
import axios from 'axios';    
  export default {
    data: function () {
      return {
        message: "This is the home, sign in/sign up page",
        data: []
      };
    },
    created: function () {
      axios.get("http://localhost:3000/live_stream_tweets").then(response => {
        console.log(response.data)
        this.data = response.data
      })

    },
    methods: {
      stopIndex: function () {
        console.log('hello')
        axios.get("http://localhost:3000/live_stream_tweets/destroy").then(response => {
        console.log("hello")
      })
      }
    },
  };
</script>