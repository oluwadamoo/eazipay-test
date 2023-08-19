
<template>
    <div class="min-w-[272px] w-[272px] relative bg-[#fff] shadow pb-[268px]">
        <div class="relative flex items-center justify-center h-[150px]">
            <WhiteLogo :extraClass="'w-[124.335px] h-[32.66px] z-[1000]'" />
            <div class="absolute top-[0px] w-full h-full  left-0 right-0">
                <img src="/images/dashboard-mask.svg" alt="mask" class="" />
                <img src="/images/dashboard-mask2.svg" alt="mask" class="mt-[-200px]" />
            </div>

        </div>

        <div class="bg-[#fff] py-[50px] w-full ">
            <nuxt-link to="/#" v-for="(item, index) in sidebarItem" :key="index"
                class='flex items-center w-[100%] justify-between px-[20px] py-[16px] border-t-[0.8px] border-t-[#E7E8E7]'
                :class="index === 0 ? 'text-[#11453B] bg-[#F0F7EB80]' : item.label === 'Support' && 'mt-[48px]'">
                <div class="flex items-center">
                    <img :alt="item.label" :src="item.icon" />
                    <span class="ml-[12px] text-[#515251] text-[16px]">{{ item.label }}</span>
                </div>

                <img v-if="item.hasExtra" src="/images/caret-down.svg" />
            </nuxt-link>
        </div>
    </div>
</template>

<script>
import WhiteLogo from './icons/WhiteLogo.vue';



export default {
    name: 'Sidebar',
    data: () => ({
        sidebarItem: [
            {
                icon: '/images/dashboard.svg',
                label: 'Dashboard'
            },
            {
                icon: '/images/wallet.svg',
                label: 'Wallet'
            },
            {
                icon: '/images/employee.svg',
                label: 'Employee Management',
                hasExtra: true
            },
            {
                icon: '/images/payroll.svg',
                label: 'Payroll',
                hasExtra: true
            },
            {
                icon: '/images/compliance.svg',
                label: 'Compliance',
                hasExtra: true
            },
            {
                icon: '/images/loan.svg',
                label: 'Quick Loan',
                hasExtra: true
            },
            {
                icon: '/images/book-keeping.svg',
                label: 'Book Keeping',
                hasExtra: true
            },
            {
                icon: '/images/support.svg',
                label: 'Support',
            },
            {
                icon: '/images/setting.svg',
                label: 'Settings',
                hasExtra: true
            },
        ]
    }),
    components: { WhiteLogo }
}
</script>


<style scoped>
.shadow {
    box-shadow: 4px 0px 25px 0px rgba(170, 170, 170, 0.08);
}
</style>