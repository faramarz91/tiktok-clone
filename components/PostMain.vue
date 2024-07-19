<template>
    <div class="pt-[80px] w-[calc(100%-90px)] max-w-[690px]">
        <div id="PostMain" class="flex border-b py-6">
            <div class="cursor-pointer">
                <img class="rounded-full max-h-[60px]" width="60px" src="https://picsum.photos/300?random=3" alt="">
            </div>
            <div class="pl-3 w-full px-4">
                <div class="flex items-center justify-between pb-0.5">
                    <button>
                        <span class="font-bold hover:underline cursor-pointer">User Name</span>
                        <span class="text-[13px] text-light text-gray-500 pl-1 cursor-pointer">User Name</span>
                    </button>
                    <button
                        class="border text-sm px-4 py-0.5 border-[#F02C56] text-[#F02C56] hover:bg-[#FFeeF2] font-semibold rounded-md">
                        Follow
                    </button>
                </div>
                <div class="text-sm pb-0.5 break-words md:max-w-[400px] max-w-[300px]">
                    This is some text
                </div>
                <div class="text-xs text-gray-500 pb-0.5 ">
                    <span class="mr-1">#fun</span>
                    <span class="mr-1">#cool</span>
                    <span class="mr-1">#doublecool</span>
                </div>
                <div class="text-xs pb-0.5 flex items-center font-semibold">
                    <Icon name="mdi:music" size="17"/>
                    <div class="px-1">original sound - AWESOME</div>
                    <Icon name="mdi:heart" size="20"/>
                </div>
                <div class="mt-2.5 flex">
                    <div
                        class="relative min-h-[480px] max-h-[680px] max-w-[580px] flex items-center bg-black rounded-xl cursor-pointer"
                    >
                        <video
                            ref="video" loop muted
                            class="rounded-xl object-cover mx-auto h-full"
                            src="/216696_small.mp4"
                        />
                        <img
                            class="absolute right-2 bottom-14"
                            width="90"
                            src="~/assets/images/tiktok-logo-white.png"
                        >
                    </div>
                    <div class="relative mr-[75px]">
                        <div class="absolute bottom-0 pl-2">
                            <div class="pb-4 text-center">
                                <button class="rounded-full bg-gray-200 p-2 cursor-pointer hover:bg-gray-300 transition duration-200 ease-in-out">
                                    <Icon name="mdi:heart" size="25" class="text-[#F02C56] line-clamp-none"/>
                                </button>
                                <span class="text-xs text-gray-800 font-semibold">12 k</span>
                            </div>
                            <div class="pb-4 text-center">
                                <div class="rounded-full bg-gray-200 p-2 cursor-pointer hover:bg-gray-300 transition duration-200 ease-in-out">
                                    <Icon name="bx:bxs-message-rounded-dots" size="25" class="line-clamp-none"/>
                                </div>
                                <span class="text-xs text-gray-800 font-semibold">43</span>
                            </div>

                            <div class="text-center">
                                <div class="rounded-full bg-gray-200 p-2 cursor-pointer hover:bg-gray-300 transition duration-200 ease-in-out">
                                    <Icon name="ri:share-forward-fill" size="25" class="line-clamp-none"/>
                                </div>
                                <span class="text-xs text-gray-800 font-semibold">55</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
const video = ref()
onMounted(()=>video.value.play())
</script>
