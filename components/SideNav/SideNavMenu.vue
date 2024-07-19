<template>
    <NuxtLink to="/">
        <MenuItem name="mdi:home-outline" color="#F02C56" size="30">For You</MenuItem>
    </NuxtLink>
    <MenuItem name="ci:group" color="#000000" >Following</MenuItem>
    <MenuItem name="ri:live-line" >LIVE</MenuItem>
</template>
<script setup>

import MenuItem from "~/components/SideNav/MenuItem.vue";
</script>