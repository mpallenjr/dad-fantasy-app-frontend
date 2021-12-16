<template>
  <div class="home">
    <h1>{{ message }}</h1>
   <a href="dashboard"> <button> Get Started</button></a>
   
  </div>
</template>

<style></style>

<script>
  export default {
    data: function () {
      return {
        message: "click the button to find your edge",
      };
    },
    created: function () {},
    methods: {},
  };
</script>