<template>
  <div class="home">
    <pre> 
<div v-for="tweet in stream_tweets">
						{{ tweet.data }}
					</div>

    </pre>

  </div>
</template>

<style>
pre {
  max-height: 300px;
  overflow-y: auto;
}

pre[class] {
  max-height: 100px;
}

.scroll-100 {
  max-height: 100px;
  overflow-y: auto;
  background-color: inherit;
}
</style>

<script>
import axios from 'axios';
  export default {
    data: function () {
      return {
        message: "This is the home, sign in/sign up page",
        				stream_tweets: []

      };
    },
    created: function () {
      setInterval( () => { 
				axios.get("http://localhost:3000/live_stream_echos").then(response => {
					// debugger;
        	console.log(response.data)
					// if response.data is the last element of the array dont push (can also manipulate array amount here)
					
					this.stream_tweets.push(response.data);
					
					console.log("add to stream")
					console.log(this.stream_tweets)
			
     		})
			},5000)
    },
    methods: {
    },
    
  };
</script>