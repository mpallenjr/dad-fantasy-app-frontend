<template>
  <div class="home">
    <h1>{{ message }}</h1>
     <VueRssFeed :feedUrl="nflRotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="nbaRotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="rotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="ffaNewsFeed" :name="name" :limit="ffalimit"/>
     <VueRssFeed :feedUrl="dynastyNerdsNewsFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="sleeperUNewsFeed" :name="name" :limit="sleeperUlimit"/>
     <VueRssFeed :feedUrl="playerProfilerFeed" :name="name" :limit="playerProfilerlimit"/>
     <VueRssFeed :feedUrl="hoopsHypeNewsFeed" :name="name" :limit="hoopsHypeNewslimit"/>
     <VueRssFeed :feedUrl="hoopDoctorsNewsfeed" :name="name" :limit="hoopDoctorsNewslimit"/>
     <VueRssFeed :feedUrl="basketballInsidersNewsfeed" :name="name" :limit="basketballInsidersNewslimit"/>

  </div>
</template>

<style></style>

<script>
  import VueRssFeed from "vue-rss-feed";
  export default {
    name: "Demo",
    components: {
    VueRssFeed
  },
    data: function () {
      return {
        message: "This is the dashboard",
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
        basketballInsidersNewslimit: 10

      };
    },
    created: function () {},
    methods: {},
  };
</script>