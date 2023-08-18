<template>
    <nuxt-link to="#" class="bg-[#fff] shadow px-[24px] flex flex-col items-center py-[16px] rounded-[24px]">
        <div :class="color" class="flex items-center justify-center w-[48px] h-[48px] rounded-[12px]">
            <img :alt="label" :src="icon" />
        </div>

        <p class="text-[14px] text-[#515251] mt-[15.5px]">{{ label }}</p>
    </nuxt-link>
</template>

<script>

export default {
    props: ['color', 'label', 'icon'],

}
</script>

<style scoped>
.shadow {
    box-shadow: 0px 9px 18px 0px rgba(170, 170, 170, 0.15);
}
</style>