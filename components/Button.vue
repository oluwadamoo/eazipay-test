<template>
    <button @click="handleClick" :type="type ? type : 'button'" class="hover px-[32px] py-[10px] rounded-[24px] text-[14px]"
        :class="extraClass">
        {{ label }}
    </button>
</template>

<script>

export default {
    props: ['extraClass', 'label', 'type'],
    methods: {
        handleClick() {
            this.$emit('on-click', 'Hello')
        }
    }
}
</script>

