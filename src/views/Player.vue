<template>
  <div id="main">
    <br/>
    <section>
      <h3>Player Search</h3>
      <form method="post" action="#">
        <div class="row gtr-uniform">
          <div class="col-6 col-12-xsmall">
            <input type="text" name="name" id="first-name" value="" placeholder="First Name" v-model="inputPlayerData.firstName" />
          </div>
          <div class="col-6 col-12-xsmall">
            <input type="text" name="name" id="last-name" value="" placeholder="Last Name" v-model="inputPlayerData.lastName" />
          </div>
        </div>
      </form>
    </section>
    <button class="center" v-on:click="searchPlayers()">Search</button>
    <hr/>

    <form>
      <h3>Recent Tweets</h3>
      <div  v-for="tweet in inputPlayerTweetResults">
        <table>
          <!-- <thead>
            <tr>
              <th>Recent Tweets</th>
            </tr>
          </thead> -->
          <tbody>
            <tr>							
              <td>{{tweet.text}}</td>	
            </tr>			
          </tbody>
        </table>
      </div>
      <div v-for="result in inputPlayerResults" class="headlines" >
      <h2><a v-bind:href="result.url" target="_blank">{{result.title}} <a/>| {{result.author}} - {{result.source.name}} </h2>
      <p><span class="image left"><img v-bind:src="result.urlToImage" v-bind:alt="result.description" width=125 height=125></span>{{result.description}}</p>
      <br />
      <br />
      <br />
      </div>
    </form>							
  </div>
</template>

<style>

input {
    width: 250px;
    padding: 5px;
}
</style>

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
  axios.get(`https://infinite-meadow-34805.herokuapp.com/player_news_headlines?first_name=${this.inputPlayerData.firstName}&last_name=${this.inputPlayerData.lastName}`).then(response => {
    this.inputPlayerResults = response.data.articles
  }),
  axios.get(`https://infinite-meadow-34805.herokuapp.com/player_twitter_keywords?first_name=${this.inputPlayerData.firstName}&last_name=${this.inputPlayerData.lastName}`).then(response => {
    console.log(response.data)
    this.inputPlayerTweetResults = response.data.data
  })
  
}
    },
  };
</script>