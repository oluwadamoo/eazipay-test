
<template>
  <div class="pt-[95px] pb-[120px] flex items-center 2xl:px-[15%]  px-[5%] ">

    <div
      class="min-[954px]:mr-[47px] max-[954px]:text-center flex-[1] max-[954px]:flex max-[954px]:flex-col items-center">
      <h3 class="made-mellow font-[500] xl:text-[64px] text-[50px]">Run your <span class="text-[#11453B]">payroll</span>
        <span class="text-[#B4A572]">easily</span> <span class="text-[#EA4E4B]">in</span> <span>seconds</span>
      </h3>

      <p class="xl:text-[20px] text-[16px] leading-[28px] mt-[24px] text-[#515251] xl:w-[100%] min-[954px]:w-[80%]">
        We’ve built an all-inclusive simple solution for individual and businesses to manage staff, pay salaries, bills,
        and relevant taxes all at once.
      </p>

      <Button
        :extraClass="'mb-[72px] mt-[24px] px-[36px] green-btn bg-[#11453B] border-[1px] border-[#11453B] text-[#FFF]'"
        :label="'Start Using Free, Forever'" />


      <h4 class="text-[#000] text-[18px] font-[500] mb-[16px] aeonik-bold">Download the Eazipay App</h4>

      <div class="flex items-center">
        <StoreCard :icon="'apple'" :subtext="'Download on the'" :text="'Appstore'" />
        <StoreCard :subtext="'Get on'" :text="'Google Play'" :extraClass="'ml-[16px]'" />
      </div>
    </div>


    <div class="min-[954px]:block hidden relative flex-[1] 2xl:mr-[-30%] mr-[-10%]">
      <div class="mask rounded-full overflow-hidden max-w-[670.699px] max-h-[670.699px]">
        <GreenMask />
      </div>

      <div class="z-[1000] absolute top-[10%] 2xl:right-[5%] right-[-15%]">
        <MockDashboard />
      </div>

      <!-- payroll -->
      <div
        class="rounded-tr-[11.94px] rounded-br-[11.94px] rounded-bl-[11.94px] p-[11.941px] max-w-[224px] flex items-center absolute top-[0] bg-[#fff] shadow left-[0]">
        <div class="bg-[#11453B] p-[8px] rounded-full flex items-center justify-center">
          <Mark />

        </div>
        <p class="text-[11.941px] ml-[10px] text-[#515251]">Simplify payroll with Eazipay's one-click solution!</p>
      </div>

      <!-- Join Businesses -->
      <div
        class="rounded-tr-[11.94px] rounded-tl-[11.94px]  rounded-bl-[11.94px] p-[11.941px] max-w-[224px] flex items-center absolute top-[40%] bg-[#fff] shadow left-[-10%]">
        <div class="bg-[#11453B] p-[8px] rounded-full flex items-center justify-center">
          <BusinessIcon />

        </div>
        <p class="text-[11.941px] ml-[10px] text-[#515251]">Join <span class="text-[#EA4E4B]">200+</span> businesses using
          Eazipay's easy solution.</p>
      </div>
      <div
        class="z-[1000000] rounded-tr-[11.94px] rounded-br-[11.94px] rounded-bl-[11.94px] p-[11.941px] w-[300px] flex items-center absolute bg-[#fff] shadow left-[0] bottom-[17%]">
        <img src="~static/images/bola.png" alt="bola" class="h-[33px] w-[33px]" />

        <div class=" ml-[10px] flex-[1]">
          <h5 class="text-[20px] mb-[2px] text-[#292A29]">Bolade Ifedayo</h5>
          <p class="text-[12px] text-[#515251]">Data Analyst</p>

          <div class="flex justify-between items-center">
            <p class="text-[12px] text-[#515251]">Female | Monthly</p>
            <p class="text-[16px] text-[#11453B] aeonik-bold">N250,600.78</p>

          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
import GreenMask from './icons/GreenMask.vue';
import MockDashboard from './icons/MockDashboard.vue';
import Mark from './icons/Mark.vue';
import BusinessIcon from './icons/BusinessIcon.vue';


export default {
  name: 'LandingPageHero',
  components: { GreenMask, MockDashboard, Mark, BusinessIcon },
  data: () => ({

  }),
}
</script>


<style>
.mask {
  background: radial-gradient(83.29% 55.00% at 50.00% 50.00%, #227565 0%, #072B24 100%);
}
</style>