<template>
  <div>
    <nav-bar />
    <section class="main-content">
      <nuxt />
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import NavBar from '~/components/NavBar.vue';

export default Vue.extend({
  components: { NavBar },
});
</script>
