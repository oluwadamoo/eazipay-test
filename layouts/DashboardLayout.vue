<template>
    <div class="flex">
        <Sidebar />
        <main class="flex-[1]">
            <DashboardNav />
            <div class="h-[80px]" />
            <Nuxt />
        </main>
    </div>
</template>

<script>
import Sidebar from '@/components/Sidebar.vue'
import DashboardNav from '~/components/DashboardNav.vue';

export default {
    components: {
        Sidebar,
        DashboardNav
    }
}

</script>