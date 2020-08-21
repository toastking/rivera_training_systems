<template>
  <div>
    <b-navbar type="is-primary">
      <template slot="brand">
        <b-navbar-item tag="router-link" :to="{ path: '/' }" class="is-size-3">
          <span class="has-text-weight-bold is-italic">Rivera</span>
          <span>&nbsp;</span>
          <span>Training Systems</span>
        </b-navbar-item>
      </template>
      <template slot="end">
        <b-navbar-item
          v-scroll-to="'#how-we-work'"
          tag="a"
          href="#"
          class="is-italic has-text-weight-semibold"
        >
          How We Work
        </b-navbar-item>
        <b-navbar-item
          v-scroll-to="'#services'"
          tag="a"
          href="#"
          class="is-italic has-text-weight-semibold"
        >
          What We Do
        </b-navbar-item>
        <b-navbar-item
          v-scroll-to="'#bios'"
          tag="a"
          href="#"
          class="is-italic has-text-weight-semibold"
        >
          Who We Are
        </b-navbar-item>
        <b-navbar-item
          v-scroll-to="'#testimonials'"
          tag="a"
          href="#"
          class="is-italic has-text-weight-semibold"
        >
          Client Stories
        </b-navbar-item>
      </template>
    </b-navbar>

    <section class="main-content">
      <nuxt />
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>
