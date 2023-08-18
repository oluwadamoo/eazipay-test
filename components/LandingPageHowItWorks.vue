
<template>
    <div class=" 2xl:px-[15%]  px-[5%] bg-[#FFF] flex flex-col items-center text-center py-[93px]">
        <h4 class="made-mellow xl:text-[64px] text-[40px] mb-[16px] text-[#11453B]">How Eazipay Works</h4>
        <p class="xl:text-[20px] text-[16px] text-[#292A29]">Get started in 3 simple steps.</p>

        <div class="flex my-[100px] w-[100%] justify-center">

            <div class="relative">

                <div class="bigger-elipsis flex items-center justify-center h-[577.149px] w-[577.149px] rounded-full">
                    <div class="big-elipsis flex items-center justify-center h-[518.158px] w-[518.158px] rounded-full">
                        <div class="elipsis h-[450.897px] w-[450.897px] rounded-full"></div>
                    </div>
                </div>

                <div
                    class="absolute top-[-10%] left-[20%] overflow-hidden rounded-[63.267px] h-[690px] w-[355px] bg-[#11453B] flex items-center justify-center">
                    <img src="~static/images/onboarding.gif" alt="onboarding"
                        class="min-h-[682px] h-[682px] min-w-[347.61px] w-[347.61px]" />
                </div>
            </div>

            <div class="ml-[100px] relative w-[50%] min-[954px]:block hidden">
                <!-- Step 1 -->
                <div class="flex">
                    <img src="/images/create-left.svg" alt="create free account" class="mt-[4%]" />
                    <div class="flex flex-col items-start">
                        <div
                            class="rounded-[16px] h-[64px] w-[64px] flex items-center justify-center bg-[#11453B] text-[#fff] aeonik-bold text-[36px]">
                            1</div>
                        <div class="mt-[16px]">


                            <h4 class="aeonik-bold text-[20px] text-left">Create your free account</h4>
                            <p class="text-[16px] text-[#515251] mt-[16px] text-left">Click here to set up your Eazipay
                                account
                            </p>
                        </div>
                    </div>
                </div>

                <!-- step 2 -->
                <div class="ml-[50px] mt-[-45px] ">
                    <div class="flex flex-col items-start">
                        <div
                            class="rounded-[16px] h-[64px] w-[64px] flex items-center justify-center bg-[#F2F1F1] text-[#11453B] aeonik-bold text-[36px]">
                            2</div>
                        <div class="mt-[16px]">


                            <h4 class="aeonik-bold text-[20px] text-left">
                                Add Employee Data</h4>
                            <p class="text-[16px] text-[#515251] mt-[16px] text-left max-w-[80%]">
                                Your employee information is 100% safe and secure.
                            </p>
                        </div>
                    </div>

                    <img src="/images/add-right.svg" alt="create free account" class="mt-[-25%] ml-[15%]" />

                </div>

                <!-- Step 3 -->
                <div class="mt-[-45px] ml-[40px]">
                    <div class="flex flex-col items-start">
                        <div
                            class="rounded-[16px] h-[64px] w-[64px] flex items-center justify-center bg-[#F2F1F1] text-[#11453B] aeonik-bold text-[36px]">
                            3</div>
                        <div class="mt-[16px]">


                            <h4 class="aeonik-bold text-[20px] text-left">
                                Prepare your Transaction</h4>
                            <p class="text-[16px] text-[#515251] mt-[16px] text-left max-w-[80%]">
                                Run payroll: Bulk Salaries and Compliance are done at once! </p>
                        </div>
                    </div>


                </div>

            </div>
        </div>
    </div>
</template>

<script>


export default {
    name: 'LandingPageHowItWorks',
    data: () => ({

    }),
}
</script>


<style>
.bigger-elipsis {
    border: 0.187px solid #11453B;
    background: #F0F7EB;
}

.big-elipsis {
    background: #D9EBCD
}

.elipsis {
    background: #11453B;
}
</style>