<template>
    <nav
        class="z-[100000] bg-[#fff] fixed w-[calc(100%-272px)] top-[0] flex px-[61px] items-center justify-between h-[80px] shadow">
        <img alt="company logo" src="/images/f-logo.svg" />

        <div class="flex items-center">

            <button class="relative w-fit">
                <img alt="notification" src="/images/bell.svg" />

                <div
                    class="text-[10px] text-[#fff] aeonik-bold absolute top-[-6px] right-[-4px] bg-[#C92F02] w-[16px] h-[16px] rounded-full flex items-center justify-center">
                    2</div>
            </button>

            <button class="flex items-center ml-[68px]">
                <img src="/images/user.svg" />
                <div class="text-left mx-[17px]">
                    <h6 class="aeonik-bold text-[16px] ">Kalu Abasiama</h6>
                    <p class="text-[#898989] text-[14px]">Admin</p>
                </div>

                <img alt="user" src="/images/caret-down.svg" class="-rotate-90" />
            </button>
        </div>
    </nav>
</template>


<style scoped>
.shadow {
    box-shadow: 0px 4px 25px 0px rgba(0, 0, 0, 0.05);
}
</style>