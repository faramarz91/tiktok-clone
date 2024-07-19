<template>
    <div
        id="SideNavMain"
        :class="route.fullPath === '/' ? 'lg:w-[310px]' : 'lg:w-[220px]'"
        class="fixed z-20 bg-white pt-[70px] h-full lg:border-r-0 border-r w-[75px] overflow-auto"
    >
        <div class="lg:w-full w-[55px] mx-auto">
            <SideNavMenu/>

            <SuggestedAccount/>

            <FollowingAccount/>

            <SideNavFooter/>

        </div>
    </div>
</template>

<script setup>

import SideNavMenu from "~/components/SideNav/SideNavMenu.vue";
import SuggestedAccount from "~/components/SideNav/SuggestedAccount.vue";
import FollowingAccount from "~/components/SideNav/FollowingAccount.vue";
import SideNavFooter from "~/components/SideNav/SideNavFooter.vue";

const route = useRoute();
</script>