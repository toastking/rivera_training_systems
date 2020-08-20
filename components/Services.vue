<template>
  <section class="section has-background-blue-grey">
    <div class="columns">
      <div class="column is-full">
        <h2
          class="title is-2 has-text-white is-uppercase has-text-centered has-text-weight-semibold"
        >
          What We Do
        </h2>
      </div>
    </div>

    <div class="columns">
      <div v-for="service of services" :key="service" class="column">
        <p class="has-text-white has-text-centered is-uppercase is-size-4">
          {{ service }}
        </p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue, { PropType } from 'vue'

export default Vue.extend({
  props: {
    services: {
      type: Array as PropType<string[]>,
      required: true,
    },
  },
})
</script>
