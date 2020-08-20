<template>
  <section class="section has-background-light" id="testimonials">
    <div class="columns">
      <div class="column is-full">
        <h2
          class="is-uppercase is-italic has-text-centered has-text-primary title is-2"
        >
          Real Results
        </h2>
      </div>
    </div>
    <div class="tile is-ancestor">
      <div
        v-for="testimonial of testimonials"
        :key="testimonial.name"
        class="tile"
      >
        <div class="card">
          <div class="card-content">
            <p class="title">"{{ testimonial.testimonial }}"</p>
            <p v-if="testimonial.name !== ''" class="subtitle">
              - {{ testimonial.name }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue, { PropType } from 'vue';

/** Object representing a customer testmonial */
interface Testimonial {
  testimonial: string;
  name: string;
}

export default Vue.extend({
  props: {
    testimonials: {
      type: Array as PropType<Testimonial[]>,
      required: true,
    },
  },
});
</script>
