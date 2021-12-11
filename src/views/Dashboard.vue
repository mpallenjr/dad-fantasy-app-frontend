<template>
  <div class="home">
    <h1>{{ message }}</h1>
     <VueRssFeed :feedUrl="nflRotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="nbaRotoworldFeed" :name="name" :limit="limit"/>
     <VueRssFeed :feedUrl="rotoworldFeed" :name="name" :limit="limit"/>
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
        name: "",
        limit: 5,
        rotoworldFeed: "http://localhost:3000/rotowire_news",
        name: "",
        limit: 5
      };
    },
    created: function () {},
    methods: {},
  };
</script>