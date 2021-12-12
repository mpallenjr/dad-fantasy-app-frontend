<template>
  <div class="home">

    <!-- Main -->
        <section id="main">

          <!-- Items -->
            <div class="items">

              <div class="item intro span-2">
                <h1>Parallelism</h1>
                <p>A responsive portfolio site<br />
                template by HTML5 UP</p>
              </div>

    
            <div v-for="article in nba_articles.articles">
              <article class="item thumb span-1">
                <h2>{{ article.title }}</h2>
                <a href="" class="image"><img v-bind:src="article.urlToImage" alt=""></a>
              </article>
            </div>

            </div>

          <!-- Items -->
            <div class="items">
               <div v-for="article in nfl_articles.articles">
                <article class="item thumb span-1">
                  <h2>{{ article.title }}</h2>
                  <a href="" class="image"><img v-bind:src="article.urlToImage" alt=""></a>
                </article>
              </div>
            </div>

             <div class="items">
               <div v-for="filtered_keyword_tweet in filtered_keyword_tweets.data">
                <article class="item thumb span-1">
                  <h2>{{ filtered_keyword_tweet.text }}</h2>
                  <a href="" class="image"><img src="/images/white.png" alt=""></a>
                </article>
              </div>
            </div>

        
  <a class="btn btn-primary" data-bs-toggle="collapse" href="#rotowirenfl" role="button" aria-expanded="false" aria-controls="collapseExample">
RotoWire NFL  </a>
 |
<div class="collapse" id="rotowirenfl">
  <div class="card card-body">
     <VueRssFeed :feedUrl="nflRotoworldFeed" :name="name" :limit="limit"/>
  </div>
</div>

<a class="btn btn-primary" data-bs-toggle="collapse" href="#rotowirenba" role="button" aria-expanded="false" aria-controls="collapseExample">
RotoWire NBA  </a>
|
<div class="collapse" id="rotowirenba">
  <div class="card card-body">
    <VueRssFeed :feedUrl="nbaRotoworldFeed" :name="name" :limit="limit"/>
  </div>
</div>

<a class="btn btn-primary" data-bs-toggle="collapse" href="#rotowire" role="button" aria-expanded="false" aria-controls="collapseExample">
RotoWire</a>
|
<div class="collapse" id="rotowire">
  <div class="card card-body">
     <VueRssFeed :feedUrl="rotoworldFeed" :name="name" :limit="limit"/>
  </div>
</div>

<a class="btn btn-primary" data-bs-toggle="collapse" href="#ffa" role="button" aria-expanded="false" aria-controls="collapseExample">
Fantasy Football Analytics  </a>
|
<div class="collapse" id="ffa">
  <div class="card card-body">
     <VueRssFeed :feedUrl="ffaNewsFeed" :name="name" :limit="ffalimit"/>
  </div>
</div>

<a class="btn btn-primary" data-bs-toggle="collapse" href="#dynastynerds" role="button" aria-expanded="false" aria-controls="collapseExample">
Dyansty Nerds  </a>
|
<div class="collapse" id="dynastynerds">
  <div class="card card-body">
     <VueRssFeed :feedUrl="dynastyNerdsNewsFeed" :name="name" :limit="limit"/>
  </div>
</div>
<a class="btn btn-primary" data-bs-toggle="collapse" href="#sleeperu" role="button" aria-expanded="false" aria-controls="collapseExample">
Sleeper U </a>
|
<div class="collapse" id="sleeperu">
  <div class="card card-body">
     <VueRssFeed :feedUrl="sleeperUNewsFeed" :name="name" :limit="sleeperUlimit"/>
  </div>
</div>
<a class="btn btn-primary" data-bs-toggle="collapse" href="#playerprofiler" role="button" aria-expanded="false" aria-controls="collapseExample">
Player Profiler  </a>
|
<div class="collapse" id="playerprofiler">
  <div class="card card-body">
     <VueRssFeed :feedUrl="playerProfilerFeed" :name="name" :limit="playerProfilerlimit"/>
  </div>
</div>
<a class="btn btn-primary" data-bs-toggle="collapse" href="#hhnews" role="button" aria-expanded="false" aria-controls="collapseExample">
Hoops Hype News  </a>
|
<div class="collapse" id="hhnews">
  <div class="card card-body">
     <VueRssFeed :feedUrl="hoopsHypeNewsFeed" :name="name" :limit="hoopsHypeNewslimit"/>
  </div>
</div>
<a class="btn btn-primary" data-bs-toggle="collapse" href="#hoopdr" role="button" aria-expanded="false" aria-controls="collapseExample">
Hoop Doctor  </a>
|
<div class="collapse" id="hoopdr">
  <div class="card card-body">
     <VueRssFeed :feedUrl="hoopDoctorsNewsfeed" :name="name" :limit="hoopDoctorsNewslimit"/>
  </div>
</div>
<a class="btn btn-primary" data-bs-toggle="collapse" href="#bbinsider" role="button" aria-expanded="false" aria-controls="collapseExample">
BB Insider </a>
|
<div class="collapse" id="bbinsider">
  <div class="card card-body">
     <VueRssFeed :feedUrl="basketballInsidersNewsfeed" :name="name" :limit="basketballInsidersNewslimit"/>
  </div>
</div>


        </section>

    <!-- This is the div for the nfl articles from the NEWS API -->
    <!-- <div v-for="article in nfl_articles.articles">
    <h1>{{ article.source.name }}</h1>
    <img v-bind:src="article.urlToImage">
    <h1>{{ article.title }}</h1>
    </div> -->

    <!-- This is the div for the nba articles from the NEWS API -->
    <!-- <div v-for="article in nba_articles.articles">
    <h1>{{ article.source.name }}</h1>
    <img v-bind:src="article.urlToImage">
    <h1>{{ article.title }}</h1>
    </div> -->


 


      <!-- The RSS Feed Elements -->
     <!-- <VueRssFeed :feedUrl="nflRotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="nbaRotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="rotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="ffaNewsFeed" :name="name" :limit="ffalimit"/>
     <VueRssFeed :feedUrl="dynastyNerdsNewsFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="sleeperUNewsFeed" :name="name" :limit="sleeperUlimit"/>
     <VueRssFeed :feedUrl="playerProfilerFeed" :name="name" :limit="playerProfilerlimit"/>
     <VueRssFeed :feedUrl="hoopsHypeNewsFeed" :name="name" :limit="hoopsHypeNewslimit"/>
     <VueRssFeed :feedUrl="hoopDoctorsNewsfeed" :name="name" :limit="hoopDoctorsNewslimit"/>
     <VueRssFeed :feedUrl="basketballInsidersNewsfeed" :name="name" :limit="basketballInsidersNewslimit"/> -->

    
    <!-- <div v-for="filtered_keyword_tweet in filtered_keyword_tweets.data">
    <h1>{{ filtered_keyword_tweet.id }}</h1>
    <h1>{{ filtered_keyword_tweet.text }}</h1>
    <hr/>
    </div> -->

  </div>
</template>

<style></style>

<script>
  import axios from 'axios';
  import VueRssFeed from "vue-rss-feed";
  export default {
    name: "Demo",
    components: {
    VueRssFeed
  },
    data: function () {
      return {
        message: "This is the dashboard",
        // Start of RSS FEEDS
        nflRotoworldFeed: "http://localhost:3000/rotowire_nfl_news",
        name: "",
        limit: 5,
        nbaRotoworldFeed: "http://localhost:3000/rotowire_nba_news",
        rotoworldFeed: "http://localhost:3000/rotowire_news",
        ffaNewsFeed: "http://localhost:3000/ffa_news",
        ffalimit: 1,
        dynastyNerdsNewsFeed: "http://localhost:3000/dynasty_nerds_news",
        sleeperUNewsFeed: "http://localhost:3000/sleeper_u_news",
        sleeperUlimit: 3,
        playerProfilerFeed: "http://localhost:3000/player_profiler_news",
        playerProfilerlimit: 8,
        hoopsHypeNewsFeed: "http://localhost:3000/hoops_hype_news",
        hoopsHypeNewslimit: 10,
        hoopDoctorsNewsfeed: "http://localhost:3000/hoop_doctors_news",
        hoopDoctorsNewslimit: 1,
        basketballInsidersNewsfeed: "http://localhost:3000/basketball_insiders_news",
        basketballInsidersNewslimit: 10,
        // End of Rss Feeds
        nfl_articles: [],
        nba_articles: [],
        filtered_keyword_tweets: [],

        

      };
    },
    created: function () {
      // NEWS API Calls to Backend
     axios.get("http://localhost:3000/nfl_news.json").then(response => {
        console.log(response.data)
        this.nfl_articles = response.data
      }),
      axios.get("http://localhost:3000/nba_news.json").then(response => {
        console.log(response.data)
        this.nba_articles = response.data
      }),
      // Twitter API calls to Backend     
      axios.get("http://localhost:3000/filtered_keyword_tweets").then(response => {
      console.log(response.data)
      this.filtered_keyword_tweets = response.data
      })

        
      
    },
    methods: {},
    mounted: function () {

      
    }
  };
</script>