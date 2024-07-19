<template>
    <div class="w-full flex items-center hover:bg-gray-100 p-2.5 rounded-md">
        <div class="flex items-center lg:mx-0 mx-auto">
            <Icon :name="name" :style="`color: ${color}`" :size="size" :class="`text-[${color}]`"/>
            <span
                :class="`text-[${color}]`"
                class="lg:block hidden pl-[9px] mt-0.5 font-semibold text-[17px]"
            >
                <slot/>
            </span>
        </div>
    </div>
</template>

<script setup>
defineProps({
    name: {type: String, required: false},
    size: {type: String, default: '27'},
    color: {type: String, default: '#000000'},
})
</script>