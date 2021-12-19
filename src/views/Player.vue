<template>
  <div class="home">
   <p>first name:  <input type="text" v-model="inputPlayerData.firstName"> </p>
   <p>last name:  <input type="text" v-model="inputPlayerData.lastName"> </p>
   <button v-on:click="searchPlayers()">Search</button>
    
    <div v-for="tweet in inputPlayerTweetResults">
     <p> {{tweet.text}}</p>
    </div>
    <div v-for="result in inputPlayerResults">
      {{result.source.name}}
      {{result.author}}
      {{result.title}}
      {{result.description}}
      <img v-bind:src="result.urlToImage">
    </div>
  </div>
</template>

<style></style>

<script>
import axios from 'axios';
  export default {
    data: function () {
      return {
        inputPlayerData: [],
        inputPlayerResults: [],
        inputPlayerTweetResults: []
      };
    },
    created: function () {},
    methods: {
searchPlayers: function () {
  console.log(this.inputPlayerData.firstName, this.inputPlayerData.lastName)
  axios.get(`http://localhost:3000/player_news_headlines?first_name=${this.inputPlayerData.firstName}&last_name=${this.inputPlayerData.lastName}`).then(response => {
    this.inputPlayerResults = response.data.articles
  }),
  axios.get(`http://localhost:3000/player_twitter_keywords?first_name=${this.inputPlayerData.firstName}&last_name=${this.inputPlayerData.lastName}`).then(response => {
    console.log(response.data)
    this.inputPlayerTweetResults = response.data.data
  })
  
}
    },
  };
</script>