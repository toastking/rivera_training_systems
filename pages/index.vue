<template>
  <div>
    <hero />
    <services :services="landingPage.services" />
    <mission-statement :mission="landingPage.mission" />
    <bios :bios="landingPage.bios" />
    <testimonials :testimonials="landingPage.testimonials" />
    <contact />
    <site-footer />
  </div>
</template>

<script lang="ts">
import Hero from '~/components/Hero.vue';
import Services from '~/components/Services.vue';
import Bios from '~/components/Bios.vue';
import Testimonials from '~/components/Testimonials.vue';
import Contact from '~/components/Contact.vue';
import SiteFooter from '~/components/SiteFooter.vue';
import MissionStatement from '~/components/MissionStatement.vue';

import { Context } from '@nuxt/types';

export default {
  name: 'HomePage',
  components: {
    Hero,
    Services,
    Bios,
    Testimonials,
    Contact,
    SiteFooter,
    MissionStatement,
  },
  async asyncData(context: Context) {
    const landingPage = await context.$content('pages', 'landingpage').fetch();
    return { landingPage };
  },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' },
      ],
    };
  },
};
</script>
