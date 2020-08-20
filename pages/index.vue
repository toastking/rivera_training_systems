<template>
  <div>
    <hero />
    <how-we-work />
    <services :services="landingPage.services" />
  </div>
</template>

<script lang="ts">
import Hero from '~/components/Hero.vue'
import HowWeWork from '~/components/HowWeWork.vue'
import Services from '~/components/Services.vue'
import { Context } from '@nuxt/types'

export default {
  name: 'HomePage',
  components: { Hero, HowWeWork, Services },
  async asyncData(context: Context) {
    const landingPage = await context.$content('pages', 'landingpage').fetch()
    return { landingPage }
  },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' },
      ],
    }
  },
}
</script>
