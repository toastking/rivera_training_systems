<template>
  <section class="section" id="how-we-work">
    <div class="columns has-background-white">
      <div class="column is-full">
        <h2
          class="is-uppercase is-italic has-text-centered has-text-primary title is-2"
        >
          What We Do
        </h2>
      </div>
    </div>
    <div class="columns has-background-white is-centered">
      <div
        v-for="service of services"
        :key="service.service"
        class="column is-narrow"
      >
        <figure class="image is-4by3">
          <img :src="service.image" />
        </figure>
        <p
          class="is-uppercase is-italic has-text-centered has-text-primary is-size-4 has-text-weight-semibold"
        >
          {{ service.service }}
        </p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue, { PropType } from 'vue';

/** Service that the trainers offer */
interface Service {
  service: string;
  image: string;
}

export default Vue.extend({
  props: {
    services: {
      type: Array as PropType<Service[]>,
      required: true,
    },
  },
});
</script>
