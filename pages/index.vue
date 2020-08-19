<template>
  <div>
    <hero />
    <how-we-work />
  </div>
</template>

<script>
import Hero from '~/components/Hero.vue'
import HowWeWork from '~/components/HowWeWork.vue'

export default {
  name: 'HomePage',
  components: { Hero, HowWeWork },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' },
      ],
    }
  },
}
</script>
