<template>
  <div>
    <b-navbar type="is-primary" :shadow="true">
      <template slot="brand">
        <b-navbar-item tag="router-link" :to="{ path: '/' }">
          <img
            src="~/assets/buefy.png"
            alt="Lightweight UI components for Vue.js based on Bulma"
          />
        </b-navbar-item>
      </template>
      <template slot="end">
        <b-navbar-item>How We Work</b-navbar-item>
        <b-navbar-item>Who We Are</b-navbar-item>
        <b-navbar-item>Client Stories</b-navbar-item>
      </template>
    </b-navbar>

    <section class="main-content">
      <div class="container">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>
