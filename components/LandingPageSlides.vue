
<template>
  <div class="relative 2xl:px-[15%] bg-transparent px-[5%] flex flex-col items-center text-center py-[190px]">

    <div class=" absolute left-[0] right-[0] top-[0] bottom-[0] z-[-1] h-[100%]">
      <img src="/images/wave.png" class="w-full h-full" />
    </div>
    <h4 class="made-mellow xl:text-[64px] text-[40px] mb-[16px] text-[#11453B]">For Individuals and Businesses</h4>
    <p class="xl:text-[20px] text-[16px] text-[#292A29]">Join 200+ businesses using Eazipay's easy solution.</p>

    <!-- CARDS -->
    <div class="flex items-center relative h-[350px] my-[20px] w-[100%]">
      <LandingAboutCard :label="'Tamper-proof Payroll for LIfe'"
        :details="`Your staff payroll history is kept in one place forever.\n\nNo more excel sheet or manual records.\n\nDownload your payroll history anytime you need it.`"
        :extra-class="'tamper  left-[0]'" />

      <LandingAboutCard :label="'All Payroll, Anytime Anywhere'"
        :extra-class="'z-[90] absolute xl:right-[30%] right-[20%] payroll'"
        :details="`Wherever you are Eazipay has got you covered on ALL your Payroll tasks.\n\nWhether it is Taxes, Pension insurances HMOs, trustfunds, Eazipay handle all your compliamces in one place and easily, in seconds!`" />

      <LandingAboutCard :extra-class="'insec z-[100] absolute right-[0]'" :label="'Payroll in Seconds'"
        :details="`Never again wil you spend more than 2 minutes on payroll.\n\nJust click on your staff annd bulk-pay them at once.\n\nPayment is done permanently.`" />
    </div>

    <p class="xl:text-[20px] text-[14px] text-[#515251] max-w-[621px]">
      We are happy to answer your queries. Please, reach us at <a href="mailto:hello@myeazipay.com"
        class="text-[#EA4E4B]"> hello@myeazipay.com</a> and expect our response shortly after.
    </p>

  </div>
</template>

<script>
import GreenMask from './icons/GreenMask.vue';
import MockDashboard from './icons/MockDashboard.vue';
import Mark from './icons/Mark.vue';
import BusinessIcon from './icons/BusinessIcon.vue';
import LandingAboutCard from './LandingAboutCard.vue';


export default {
  name: 'LandingPageSlides',
  components: { GreenMask, MockDashboard, Mark, BusinessIcon, LandingAboutCard },
  data: () => ({

  }),
}
</script>


<style>
.tamper {
  transition: all 0.4s ease-in-out;
}



.tamper:hover+.payroll {
  animation: tamperAnim 0.3s linear both;

  @media (max-width: 954px) {
    animation: tamperAnimSm 0.3s linear both;
  }

}

.tamper:hover {
  @media (max-width: 954px) {
    position: absolute;
    animation: tamperSm 0.3s linear both;
  }

}

.payroll:hover {
  animation: payrollAnim 0.3s linear forwards;

  @media (max-width: 954px) {
    position: absolute;
    animation: payrollAnimSm 0.3s linear both;
  }
}

.tamper:hover+.insec {
  @media (max-width: 954px) {
    animation: insecAnimSm 0.3s linear both;
  }

}

@keyframes insecAnimSm {

  to {
    right: 10%
  }
}

@keyframes tamperSm {

  to {
    left: -7%
  }
}

@keyframes tamperAnim {

  to {
    right: 20%
  }


}

@keyframes tamperAnimSm {

  to {
    right: 1%
  }
}

@keyframes payrollAnim {

  to {
    right: 40%
  }
}

@keyframes payrollAnimSm {

  to {
    right: 50%
  }
}
</style>