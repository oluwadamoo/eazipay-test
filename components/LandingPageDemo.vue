
<template>
  <div class="relative 2xl:px-[15%] bg-[#FFF] px-[5%]  py-[190px]">

    <img src="/images/hor-dots.svg" class="absolute left-[0] top-[5%] xl:w-[auto] w-[100px]" />

    <div class="flex  max-[954px]:flex-col">
      <div class=" max-[954px]:mb-[24px]">
        <h2 class="made-mellow xl:text-[64px] md:text-[54px] text-[40px] mb-[24px] text-left text-[#11453B]">Get an
          Exclusive Demo of Eazipay </h2>

        <p class="xl:text-[24px] text-[16px] text-[#515251]  max-[954px]:text-center">Our greatest priority is to put you
          and your business first.
          Let’s show you
          how we can help.</p>
      </div>

      <form class="ml-[24px] border-[1px] shadow-lg p-[32px] rounded-[32px]">
        <h5 class="text-[28px] text-center aeonik-bold text-[#292A29] mb-[12px]">First things first</h5>
        <p class="text-center text-[18px] text-[#444444]">We want to serve you better. Tell us a bit about yourself or
          company</p>

        <div class="border-[1px] p-[8px] flex rounded-[16px] my-[24px] border-[#F2F1F1]">
          <Button v-for="(tab, index) in tabs" @on-click="changeTab(tab)" :key="index"
            :extraClass="`w-[50%] rounded-[12px] ${tab === 'Individual' && 'mr-[12px]'} ${currentTab === tab ? 'green-btn bg-[#11453B] text-[#FFF]' : 'white-btn text-[] bg-[#fff]'} border-[1px] border-[#11453B] `"
            :label="tab" />
        </div>

        <div class="input-container border-[1px] border-[#B5B6B5] rounded-[16px]">
          <input type="text" class="floating-input outline-none" v-model="onboardingData.firstName"
            @focus="firstNameFocused = true" @blur="firstNameFocused = false">
          <label class="floating-label" :class="{ focused: firstNameFocused || onboardingData.firstName }">First
            Name</label>
        </div>
        <div class="input-container border-[1px] border-[#B5B6B5] rounded-[16px]">
          <input type="text" class="floating-input outline-none" v-model="onboardingData.lastName"
            @focus="lastNameFocused = true" @blur="lastNameFocused = false">
          <label class="floating-label" :class="{ focused: lastNameFocused || onboardingData.lastName }">Last Name</label>
        </div>
        <div class="input-container border-[1px] border-[#B5B6B5] rounded-[16px]">
          <input type="email" class="floating-input outline-none" v-model="onboardingData.email"
            @focus="emailFocused = true" @blur="emailFocused = false">
          <label class="floating-label" :class="{ focused: emailFocused || onboardingData.email }">Email</label>
        </div>
        <div class="input-container border-[1px] border-[#B5B6B5] rounded-[16px]">
          <input type="text" class="floating-input outline-none" v-model="onboardingData.jobTitle"
            @focus="jobTitleFocused = true" @blur="jobTitleFocused = false">
          <label class="floating-label" :class="{ focused: jobTitleFocused || onboardingData.jobTitle }">Job
            Title</label>
        </div>

        <div class="input-container border-[1px] border-[#B5B6B5] rounded-[16px]">
          <input type="text" class="floating-input outline-none" v-model="onboardingData.companySize"
            @focus="companySizeFocused = true" @blur="companySizeFocused = false">
          <label class="floating-label" :class="{ focused: companySizeFocused || onboardingData.companySize }">Company
            Size</label>
        </div>

        <Button @on-click="requestDemo"
          :extraClass="'w-[100%] rounded-[24px] mt-[24px]  green-btn bg-[#11453B] border-[1px] border-[#11453B] text-[#FFF]'"
          :label="'Request Demo'" />

      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'LandingPageDemo',
  data() {
    return {
      tabs: ['Individual', 'Company'],
      currentTab: 'Individual',
      onboardingData: {
        firstName: "",
        lastName: '',
        email: '',
        companySize: '',
        jobTitle: ''
      },
      firstNameFocused: false,
      lastNameFocused: false,
      emailFocused: false,
      jobTitleFocused: false,
      companySizeFocused: false,
    };
  },
  methods: {
    changeTab(tab) {
      this.currentTab = tab
    },
    requestDemo() {
      this.onboardingData = {
        firstName: "",
        lastName: '',
        email: '',
        companySize: '',
        jobTitle: ''
      };

    }
  }
}
</script>


<style scoped>
.input-container {
  position: relative;
  margin-bottom: 20px;
}

.floating-input {
  width: 100%;
  padding: 10px;
  border-radius: 16px;
  font-size: 16px;
  transition: border-color 0.3s, box-shadow 0.3s;
}

.floating-label {
  position: absolute;

  top: 12px;
  left: 10px;
  padding: 0 5px;
  background-color: transparent;
  font-size: 14px;
  color: #999;
  pointer-events: none;
  transition: top 0.3s, font-size 0.3s, color 0.3s;
}

.focused {
  background-color: #fff;
  top: -10px;
  font-size: 13px;
  color: #8D8E8D;
}

.floating-input:focus {
  border: 1px solid #11453B;

}
</style>