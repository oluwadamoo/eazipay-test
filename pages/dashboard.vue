<template>
    <div class="overflow-x-hidden py-[45px] px-[80px]">
        <h3 class="aeonik-bold text-[36px] text-[#292A29]"> Welcome Abasiama </h3>
        <p class="mt-[8px] text-[16px] text-[#515251]">Pay and manage your employee in minutes</p>


        <div class="flex gap-[48px] mt-[40px]">
            <div>
                <div class="relative overflow-hidden p-[32px] rounded-[24px] justify-between flex  bg-[#11453BCE] w-[100%]">
                    <div>
                        <p class="text-[#D9EBCD] text-[16px] mb-[6px]">Wallet Balance</p>
                        <div class="flex items-center">
                            <h3 class="aeonik-bold text-[32px] text-[#fff]">N12,560,078.00</h3>
                            <button>
                                <img alt="hide" src="/images/eye.png" class="ml-[8px] h-[27px] w-[29px]" />
                            </button>
                        </div>
                    </div>

                    <button class="self-end h-[44px] px-[28px] rounded-[24px] bg-[#D9EBCD] text-[#11453B] text-[14px]">Fund
                        Wallet</button>
                    <div class="absolute top-0 left-0 z-[-1]">
                        <img alt="pattern" src="/images/wallet-pattern.svg" />
                    </div>
                </div>

                <div class="grid mt-[48px] grid-cols-4 gap-[32px]">
                    <DashboardWalletCard v-for="(item, index) in actions" :key="index" :icon="item.icon" :color="item.color"
                        :label="item.label" />
                </div>
            </div>

            <div class="shadow overflow-hidden rounded-[16px] w-[188px]">
                <div class="bg-[#D9EBCD] text-center py-[8px]">
                    <h6 class="aeonik-bold text-[16px]">Next Payroll</h6>
                </div>

                <div>
                    <div class="pt-[16px] pb-[43px] border-b-[1px] border-b-[#E7E8E7]">
                        <div class="flex  items-center  justify-center">
                            <img src="/images/calendar.svg" alt="calendar" />
                            <p class="ml-[4px] text-[#515251] text-[12px]">Friday</p>
                        </div>

                        <p class="text-center mt-[8px] aeonik-bold text-[18px]">09/11/2022</p>

                    </div>
                    <div class="px-[16px] py-[26px]">
                        <h6 class="text-[16px] text-[#515251]">Total Employee</h6>
                        <h3 class="aeonik-bold text-[32px] text-[#292A29]">64</h3>

                        <div class="flex">
                            <div class="w-[50%]">
                                <div class=" bg-[#11453B] h-[8px]">

                                </div>
                                <div class="mt-[4px]">
                                    <p class="text-[10px] text-[#8D8E8D]">Male</p>
                                    <p class="text-[10px] text-[#8D8E8D]">32</p>
                                </div>
                            </div>

                            <div class="w-[50%]">
                                <div class=" bg-[#EA4E4B] h-[8px]">

                                </div>
                                <div class="mt-[4px]">
                                    <p class="text-[10px] text-[#8D8E8D]">Female</p>
                                    <p class="text-[10px] text-[#8D8E8D]">32</p>
                                </div>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </div>

        <!-- Graph -->
        <div class="shadow p-[48px] mt-[48px] bg-[#fff] rounded-[16px]">

            <div class="flex items-center justify-between">
                <div>
                    <p class="text-[14px] text-[#515251]">Inflow</p>
                    <h4 class="text-[#219653] text-[28px] aeonik-bold">N1,567,552</h4>
                </div>
                <div>
                    <p class="text-[14px] text-[#515251]">Outflow</p>
                    <h4 class="text-[#EF4444] text-[28px] aeonik-bold">N1,567,552</h4>
                </div>

                <select class="outline-none text-[#11453B] text-[14px]">
                    <option>Inflow/Outflow</option>
                </select>
            </div>


            <apexchart type="area" :options="chartOptions" :series="series" />
        </div>


        <!-- Recent Activites -->
        <div class="mt-[48px]">

        </div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
import DashboardWalletCard from '~/components/DashboardWalletCard.vue';

export default Vue.extend({
    name: 'Dashboard',
    layout: 'DashboardLayout',
    components: { DashboardWalletCard },
    data: () => ({
        actions: [
            {
                label: 'Add Employee',
                icon: '/images/user-plus.svg',
                color: 'bg-[#FFEDEC]'
            },
            {
                label: 'Pay Salaries',
                icon: '/images/money.svg',
                color: 'bg-[#F0F7EB]'
            },
            {
                label: 'Pay Compliances',
                icon: '/images/compliance.svg',
                color: 'bg-[#E0F8EA]'
            },
            {
                label: 'Quick Loan',
                icon: '/images/loan.svg',
                color: 'bg-[#EDF5FF]'
            },
        ],
        chartOptions: {
            xaxis: {
                categories: ['JAN', 'FEB', 'MAR', 'APR', 'MAY', 'JUN', 'JUL', 'AUG', 'SEP', 'OCT', 'NOV', 'DEC']
            },
            dataLabels: {
                enabled: false
            },


        },
        series: [
            {
                name: 'Outflow',
                color: '#EF4444',
                data: [100, 140, 80, 51, 42, 109, 100, 42, 109, 100, 42, 109, 100]
            },
            {
                name: 'Inflow',
                color: '#219653',
                data: [122, 145, 132, 34, 52, 41, 145, 132, 34, 52, 41, 30, 180]
            },
        ]
    })

})
</script>
