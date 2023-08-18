
<template>
  <nav class=" 2xl:px-[15%] bg-transparent  px-[5%] flex items-center justify-between py-[20px]">
    <GreenLogo />

    <ul class="min-[954px]:flex hidden items-center ">
      <li v-for="(item, index) in navItems" class="ml-[48px] text-[16px] font-[500] text-[#515251]" :key="index">
        <nuxt-link :to="item.link">{{ item.label }}</nuxt-link>
      </li>
    </ul>

    <div>
      <Button :extraClass="'white-btn border-[#11453B] text-[#11453B] border-[1px]'" :label="'Log in'" />
      <Button :extraClass="'green-btn bg-[#11453B] border-[1px] border-[#11453B] text-[#FFF] ml-[24px]'"
        :label="'Register'" />
    </div>
  </nav>
</template>

<script>
import GreenLogo from './icons/GreenLogo.vue'

export default {
  components: { GreenLogo },
  name: 'LandingPageNavbar',

  data: () => ({
    navItems: [
      {
        label: 'Individual',
        link: '/#'
      },
      {
        label: 'Business',
        link: '/#'
      },
      {
        label: 'Pricing',
        link: '/#'
      },
      {
        label: 'Set your payroll',
        link: '/#'
      },
    ]
  })


}
</script>


<style></style>