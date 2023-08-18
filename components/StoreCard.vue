<template>
    <button class="min-w-[200px] rounded-[8px] p-[12px] flex items-center bg-[#fff] shadow" :class="extraClass">
        <div class="bg-[#F2F1F1] w-[48px] h-[48px] rounded-full flex items-center justify-center">
            <div v-if="icon === 'apple'">
                <AppleLogo />
            </div>
            <div v-else>
                <PlayStoreLogo />
            </div>
        </div>

        <div class="ml-[12px] flex flex-col items-start text-[#515251]">
            <h6 class="text-[12px] ">{{ subtext }}</h6>
            <h4 class="text-[18px] aeonik-bold">{{ text }}</h4>
        </div>


    </button>
</template>

<script>
import AppleLogo from './icons/AppleLogo.vue';
import PlayStoreLogo from './icons/PlayStoreLogo.vue';

export default {
    components: { AppleLogo, PlayStoreLogo },
    props: ['extraClass', 'text', 'subtext', 'icon']
}
</script>

<style>
.shadow {
    box-shadow: 0px 20px 48px 0px rgba(170, 170, 170, 0.29);
}
</style>

