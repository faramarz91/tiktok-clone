<template>
    <div
        id="TopNav"
        class="fixed bg-white z-30 flex items-center w-full border-b h-[61px]"
    >
        <div
            :class="route.fullPath === '/' ? 'max-w-[1150px]' : ''"
            class="flex justify-between items-center w-full px-6 mx-auto"
        >
            <div
                :class="route.fullPath === '/' ? 'w-[80%]' : 'lg:w-[20%] w-[70%]'"
            >
                <nuxt-link to="/">
                    <img src="~/assets/images/tiktok-logo.png" alt="tiktok" width="115">
                </nuxt-link>
            </div>

            <div
                class="hidden md:flex items-center bg-[#f1f1f2] p-1 rounded-full max-w-[380px] w-full"
            >
                <input
                    type="text"
                    class="w-full pl-3 my-2 bg-transparent placeholder-[#838383] text-[15px] focus:outline-none"
                    placeholder="Search account"
                >
                <div class="px-3 py-1 flex items-center border-l-gray-300">
                    <Icon name="ri:search-line" color="#A1A2A7" sizze="22"/>
                </div>
            </div>
            <div class="flex items-center justify-end gap-3 min-w-[275px] max-w-[320px] w-full">
                <button class="flex items-center border rounded-sm px-3 py-[6px] hover:bg-gray-100">
                    <Icon name="mdi:plus" color="#000000" size="22"/>
                    <span class="font-medium px-2 text-[15px]">Upload</span>
                </button>

                <div v-if="false" class="flex items-center">
                    <button class="flex items-center bg-[#FF3B5C] text-white border rounded-md px-3 py-[6px]">
                        <span class="mx-4 font-medium text-[15px]">Log In</span>
                    </button>
                    <Icon class="ml-3" name="mdi:dots-vertical" size="22" color="#161724" />
                </div>
                <div class="flex items-center">
                    <Icon class="ml-1 mr-4 " name="carbon:send-alt" color="#161724" size="30"/>
                    <Icon class="mr-5" name="bx:message-detail" color="#161724" size="27"/>
                    <div class="relative">
                        <button class="mt-1" @click="toggleMenu">
                            <img
                                src="https://picsum.photos/300?random=1"
                                class="rounded-full w-10"
                                alt=""
                            >
                        </button>

                        <div v-if="showMenu"
                            id="PopupMenu"
                            class="absolute bg-white rounded-lg py-1.5 w-[200px] shadow-xl border top-[43px] mt-3 -right-2"
                        >
                            <nuxt-link
                                class="flex items-center justify-start py-3 px-2 hover:bg-gray-100 cursor-pointer"
                            >
                                <Icon name="ph:user" size="20"/>
                                <span class="pl-2 font-semibold text-sm">Profile</span>
                            </nuxt-link>
                            <div
                                class="flex items-center justify-start py-3 px-1.5 hover:bg-gray-100 border-t cursor-pointer"
                            >
                                <Icon name="ic:outline-logout" size="20"/>
                                <span class="pl-2 font-semibold text-sm">Logout</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    const route = useRoute();
    const showMenu = ref(false)

    const toggleMenu = () => {
      showMenu.value = !showMenu.value;
    }
</script>