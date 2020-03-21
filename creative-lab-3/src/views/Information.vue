<template>
  <div class="home">
    <h1>Enter details here and then just sit back and relax!</h1>
    <div class="paragraph">
    <p>You might be wondering how this all works, and though it may seem complicated, it's actually quite simple! Hopefully you've chosen your dream sandwich earlier and are ready to order. You enter in your info down below so that we can locate you and better get to know you. We take this info, and this information gets sent to some sweatshop full of children somewhere in India where the sandwich will be prepared and readied for consumption. Then we ship this sandwich to your location and Walah! You're a happy customer already.</p>
    <p>Your sandwich currently has {{this.$root.$data.mySandwich}}</p>
    </div>
    <form class="pure-form">
    <fieldset>
        <legend>If you are younger than 18 years of age, use your mom's credit information</legend>

        <input type="text" placeholder="Credit Card Number">
        <input type="text" placeholder="Credit Card Pin">
        <input type="text" placeholder="Social Secuirty Number">
        <input type="text" placeholder="Phone Password">

        <button v-on:click="submitFunc()" type="button" class="pure-button pure-button-primary">Send Order</button>
    </fieldset>
</form>
    <div v-if="this.$root.$data.submitted === true">
        <p>Thank you for buying from SubbySubs! Your sandwich should arrive in 3-5 business days.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Information',
  components: {
  },
  data() {
    return {
    }
  },
    methods: {
    submitFunc() {
        this.$root.$data.submitted = true;
        this.$root.$data.mySandwich = "";
    }
  },
  computed: {
  },
}
</script>
