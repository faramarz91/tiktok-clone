<template>
    <div class="lg:block hidden text-xs text-gray-600 font-semibold pt-4 pb-2 px-2">
        Following accounts
    </div>
    <div class="lg:hidden block pt-3"/>
    <div class="cursor-pointer">
        <MenuItemFollow/>
    </div>
    <button class="lg:block hidden text-rose-600 pt-1.5 pl-2 text-[13px]">
        See more
    </button>
</template>
<script setup>

import MenuItemFollow from "~/components/SideNav/MenuItemFollow.vue";
</script>