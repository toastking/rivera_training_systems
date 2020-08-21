<template>
  <section class="hero is-medium is-dark">
    <div class="hero-body">
      <div class="container is-fullhd">
        <h1 class="title is-2">
          Reach your goals
        </h1>
        <h2 class="subtitle">
          Put down your email and we'll reach out!
        </h2>
        <form
          name="emails"
          method="post"
          data-netlify="true"
          data-netlify-honeypot="bot-field"
        >
          <input type="hidden" name="form-name" value="emails" />
          <b-field>
            <b-input
              id="email"
              name="email"
              placeholder="example@example.com"
              type="email"
              rounded
            />
            <p class="control">
              <b-button native-type="submit" class="button is-info" rounded>
                Ask The Trainers
              </b-button>
            </p>
          </b-field>
        </form>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
//The hero banner for the top of the landing page
import Vue from 'vue';
export default Vue.extend({
  data() {
    return {
      email: '',
    };
  },
  methods: {
    askButtonClick() {
      this.email = '';
      this.$buefy.snackbar.open({
        message: "Thank you! We'll reach out!",
        position: 'is-top',
      });
    },
  },
});
</script>
