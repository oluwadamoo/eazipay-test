<template>
  <div class="overflow-x-hidden">
    <LandingPageNavbar />

    <LandingPageHero />

    <LandingPageSlides />

    <LandingPageHowItWorks />
    <LandingPageFree />
    <LandingPageDemo />
    <LandingPageFooter />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import LandingPageDemo from '~/components/LandingPageDemo.vue';
import LandingPageFooter from '~/components/LandingPageFooter.vue';
import LandingPageFree from '~/components/LandingPageFree.vue';
import LandingPageHero from '~/components/LandingPageHero.vue';
import LandingPageHowItWorks from '~/components/LandingPageHowItWorks.vue';
import LandingPageSlides from '~/components/LandingPageSlides.vue';

export default Vue.extend({
  name: 'IndexPage',
  components: { LandingPageHero, LandingPageSlides, LandingPageHowItWorks, LandingPageFree, LandingPageDemo, LandingPageFooter }
})
</script>
