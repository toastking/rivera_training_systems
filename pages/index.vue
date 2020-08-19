<template>
  <hero />
</template>

<script>
import Hero from '~/components/Hero.vue'

export default {
  name: 'HomePage',
  components: { Hero },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' },
      ],
    }
  },
}
</script>
