<template>
    <div class="shadow-xl rounded-lg p-5 w-fit">
        <div class="bg-[#F1F1F1] w-56 flex justify-center rounded-lg">
            <img class="h-48" :src="props.image" alt="">
        </div>
        <h1 class="font-bold my-3">{{ props.title }}</h1>
        <div class="flex justify-between">
            <span class="bg-[#BC9667] text-white py-1 px-3 rounded-lg font-bold">${{ props.price }}</span>
            <button class="border-2 py-1 px-3 border-[#BC9667] rounded-lg hover:bg-[#BC9667] hover:text-white">ADD TO
                CART</button>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(['image', `title`, `price`])
</script>