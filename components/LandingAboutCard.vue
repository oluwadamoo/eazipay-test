<template>
    <div class="h-[320px] shadow text-[#fff] bg-[#11453B] p-[64px] text-left rounded-[16px] xl:w-[552px] w-[500px]"
        :class="extraClass">

        <h4 class="xl:text-[28px] text-[20px] aeonik-bold">{{ label }}</h4>
        <p class="xl:text-[18px] text-[14px] mt-[24px]">
            {{ details }}
        </p>
    </div>
</template>

<script>
export default {
    name: 'LandingAboutCard',
    props: ['extraClass', 'label', 'details']

}





</script>

<style  scoped>
.shadow {
    box-shadow: -11px 0px 19px 0px rgba(23, 23, 23, 0.30), 0px 13px 20px 0px rgba(23, 23, 23, 0.20);
}
</style>