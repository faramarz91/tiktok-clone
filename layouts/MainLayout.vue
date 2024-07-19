<template>
    <TopNav/>
    <div
        :class="route.fullPath==='/' ? 'max-w-[1140px]' : ''"
        class="flex justify-between mx-auto w-full lg:px-2.5 px-0"
    >
        <div class="">
            <SideNavMain/>
        </div>
        <slot/>
    </div>
</template>

<script setup>
import SideNavMain from "~/components/SideNav/SideNavMain.vue";
const route = useRoute();
</script>