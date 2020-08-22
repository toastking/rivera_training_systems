<template>
  <section class="section has-background-blue-grey" id="mission">
    <div class="columns">
      <div class="column is-full">
        <h2
          class="is-uppercase is-italic has-text-centered has-text-white title is-2"
        >
          Our Mission
        </h2>
      </div>
    </div>
    <div class="columns is-centered">
      <div class="column is-full">
        <p class="has-text-white is-size-2 has-text-weight-semibold">
          "{{ mission }}"
        </p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  props: {
    mission: {
      type: String,
      required: true,
    },
  },
});
</script>
