<template>
  <div class="home">
   first name:  <input type="text" class="center" v-model="inputPlayerData.firstName"> last name:  <input type="text" class="center" v-model="inputPlayerData.lastName">
   <br/>
   <br/>
   <br/>
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
                  <h2>{{result.title}} | {{result.author}} - {{result.source.name}} </h2>
									<p><span class="image left"><img v-bind:src="result.urlToImage" v-bind:alt="result.description" width=125 height=125/></span>{{result.description}}</p>
                  <br />
                  <br />
                  <br />
                  </div>
</form>

							
  </div>
</template>

<style>

headlines
{
text-align:center;
text-justify:values;
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