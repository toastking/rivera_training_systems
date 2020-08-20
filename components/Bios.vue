<template>
  <section class="section has-background-white">
    <div class="columns">
      <div class="column is-full">
        <h2
          class="is-uppercase is-italic has-text-centered has-text-primary title is-2"
        >
          Who We Are
        </h2>
      </div>
    </div>
    <div class="columns">
      <div class="column" v-for="bio of bios" :key="bio.name">
        <figure class="image image is-128x128">
          <img :src="bio.headshot" />
        </figure>
        <h3 class="title is-3">
          <span class="has-text-weight-semibold is-uppercase">
            {{ bio.name }}
          </span>
          <span class="has-text-weight-light is-italic">
            {{ bio.credentials }}
          </span>
        </h3>
        <p>
          {{ bio.bio }}
        </p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue, { PropType } from 'vue';

/** Fields needed to show the biographical info on a trainer */
interface Bio {
  name: string;
  credentials: string;
  bio: string;
  headshot: string;
}

export default Vue.extend({
  props: {
    bios: {
      type: Array as PropType<Bio[]>,
      required: true,
    },
  },
});
</script>
