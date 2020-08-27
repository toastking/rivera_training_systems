<template>
  <section
    id="landing-hero"
    class="hero is-fullheight-with-navbar is-dark is-mobile video"
  >
    <div class="hero-video">
      <video playsinline autoplay muted loop>
        <source :src="herovideo" type="video/mp4" />
      </video>
    </div>
    <div class="hero-body">
      <div class="container is-fluid">
        <h1 class="title is-1 rivera-hero-title">
          Reach your goals
        </h1>
        <h2 class="subtitle has-shadow rivera-hero-subtitle">
          Contact us for more information
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
              placeholder="Email"
              type="email"
              size="is-medium"
              rounded
            />
            <p class="control">
              <b-button
                native-type="submit"
                class="button is-info"
                size="is-medium"
                rounded
              >
                Submit
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
  props: {
    herovideo: { type: String, required: true },
  },
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

<style lang="scss">
@import '~bulma/sass/utilities/_all';

#landing-hero {
  @include until($tablet) {
    background-image: url('~assets/hero_image_web.jpg');
    background-position: top center;
    background-repeat: no-repeat;
    background-size: cover;
  }
}

.rivera-hero-title,
.rivera-hero-subtitle {
  text-shadow: 2px 2px black;
}
</style>
