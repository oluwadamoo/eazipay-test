
<template>
  <div class="relative 2xl:px-[15%] bg-[#ffe9e7] px-[5%]  py-[190px] overflow-x-hidden">

    <img src="/images/ver-dots.svg" class="absolute top-[0] 2xl:left-[15%] left-[5%] xl:w-[auto] h-[100px]" />

    <div class="flex max-[954px]:flex-col max-[954px]:items-center max-[954px]:flex-col-reverse">
      <div class=" max-[954px]:flex flex-col items-center">
        <h4 class="made-mellow xl:text-[56px] text-[40px] mb-[16px] min-[954px]:text-left text-center text-[#11453B]">Free
          forever for
          your <span class="text-[#EA4E4B]">salary payment</span>
        </h4>

        <h4
          class="text-[#000] xl:text-[18px] text-[14px] font-[500] mb-[16px] aeonik-bold  min-[954px]:text-left text-center">
          Download the Eazipay
          App</h4>

        <div class="flex items-center ">
          <StoreCard :icon="'apple'" :subtext="'Download on the'" :text="'Appstore'" />
          <StoreCard :subtext="'Get on'" :text="'Google Play'" :extraClass="'ml-[16px]'" />
        </div>
      </div>

      <img src="/images/rimg.png" alt="man with phone" class="xl:w-[auto] w-[500px]" />
    </div>
  </div>
</template>

<script>

export default {
  name: 'LandingPageFee',
  data: () => ({

  }),
}
</script>


<style></style>