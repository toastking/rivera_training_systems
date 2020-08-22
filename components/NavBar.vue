<template>
  <b-navbar type="is-primary is-fixed-top">
    <template slot="brand">
      <b-navbar-item v-scroll-to="'#landing-hero'">
        <span
          class="has-text-weight-bold is-italic is-size-2-fullhd is-size-3-tablet"
        >
          Rivera
        </span>
        <span class="is-size-2-fullhd is-size-3-tablet">&nbsp;</span>
        <span class="is-size-2-fullhd is-size-3-tablet">Training Systems</span>
      </b-navbar-item>
    </template>
    <template slot="end">
      <b-navbar-item
        v-scroll-to="'#how-we-work'"
        tag="a"
        href="#"
        class="is-italic has-text-weight-semibold"
      >
        What We Do
      </b-navbar-item>
      <b-navbar-item
        v-scroll-to="'#mission'"
        tag="a"
        href="#"
        class="is-italic has-text-weight-semibold"
      >
        Our Mission
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
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({});
</script>
