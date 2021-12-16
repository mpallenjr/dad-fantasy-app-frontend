<template>
  <div class="home">
<div id="contact">
  <p> <form id="fs-frm" name="registration-form" accept-charset="utf-8" action="https://formspree.io/f/{form_id}" method="post" class="center">
  <fieldset id="fs-frm-inputs">
    <br />
    <br />
    <br />
    <label for="email-address" class="center">Subscribe for Updates on the App!</label>
    <br />
    <input type="email" name="_replyto" id="email-address" placeholder="email@address.com" required="">
    <input type="hidden" name="_subject" id="email-subject" value="Registration Form Submission">
  </fieldset>
  <input type="submit" value="Subscribe" class="center">
</form> </p>
</div>
  </div>
</template>

<style>
</style>

<script>
  export default {
    data: function () {
      return {
      };
    },
    created: function () {},
    methods: {},
  };
</script>