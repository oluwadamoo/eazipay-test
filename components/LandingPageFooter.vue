
<template>
  <footer
    class="2xl:px-[15%] bg-transparent  items-start px-[5%] flex  max-[954px]:flex-col-reverse  max-[954px]:items-center justify-between py-[64px] border-[1px] border-[#EAEAEA]">
    <div class="text-[14px] font-[500] text-[#515251]  mr-[125px]  max-[954px]:mt-[60px]  max-[954px]:mr-[0]">
      <GreenLogo />

      <p class="mt-[40px] text-[14px] ">
        Copyright © 2023 Eazipay.
      </p>
      <p class="text-[14px]">
        All rights reserved
      </p>

      <ul class="flex mt-[40px]">
        <li v-for="(item, index) in socialIcons" :key="index" class="mr-[16px]">
          <a :href="item.link">
            <img :alt="item.label" :src="`/images/${item.label}.svg`" />
          </a>
        </li>
      </ul>

    </div>

    <ul class="flex-[1] flex items-start justify-between  max-[954px]:justify-center  flex-wrap gap-[70px]">
      <li v-for="(item, index) in footerLinks" class=" ml-[48px] text-[16px] font-[500] text-[#515251]" :key="index">
        <p class="aeonik-bold mb-[24px]"> {{ item.title }}</p>

        <nuxt-link :to="sub.link" v-for="(sub, index) in item.items" :key="index" class="text-[14px] mb-[12px] block">
          {{ sub.label }}
        </nuxt-link>

        <div v-if="item.title.includes('Contact')"
          class="mt-[24px] flex items-center justify-between px-[16px] bg-[#F2F1F1] h-[40px] rounded-[16px] w-[255px]">
          <input placeholder="Your email address" class="outline-none h-[40px] bg-transparent" />
          <img alt="send" src="/images/send.svg" />
        </div>
      </li>
    </ul>


  </footer>
</template>

<script>
import GreenLogo from './icons/GreenLogo.vue'

export default {
  components: { GreenLogo },
  name: 'LandingPageFooter',

  data: () => ({
    footerLinks: [
      {
        title: 'Product',
        items: [
          {
            label: 'Individual',
            link: '#'
          },
          {
            label: 'Businesses',
            link: '#'
          },
          {
            label: 'Request Demo',
            link: '#'
          },
          {
            label: 'Pricing',
            link: '#'
          },
        ]
      },
      {
        title: 'Legal',
        items: [
          {
            label: 'Privacy Policy',
            link: '#'
          },
          {
            label: 'Terms of Service',
            link: '#'
          },

        ]
      },
      {
        title: 'Resources',
        items: [
          {
            label: 'FAQs',
            link: '#'
          },
          {
            label: 'Blog',
            link: '#'
          },
          {
            label: 'Career',
            link: '#'
          },
          {
            label: 'Customer Stories',
            link: '#'
          },
        ]
      },
      {
        title: 'Contact us',
        items: [
          {
            label: 'eazipay@gmail.com',
            link: '#'
          },
          {
            label: '+234 816 878 9518',
            link: '#'
          },
        ]
      },
    ],
    socialIcons: [
      {
        label: 'instagram',
        link: '/#'
      },
      {
        label: 'twitter',
        link: '/#'
      },
      {
        label: 'linkedin',
        link: '/#'
      },
      {
        label: 'facebook',
        link: '/#'
      },
    ]
  })


}
</script>


<style></style>