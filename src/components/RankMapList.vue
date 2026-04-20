<template>
    <div class="rankMap">
        <h2 class="mb-5 font-bold text-2xl"><span class="text-[#2E83C5]">{{ highlight }}</span> {{ subject }}</h2>
        <ul class="grid grid-cols-6 gap-5">
            <li v-for="item in data" :key="item.id" class="relative h-[160px] rounded-xl overflow-hidden">
                <img :src="`/src/assets/images/maps/${item.image}`" :alt="item.title" class="w-full h-full object-cover">
                <p class="absolute bottom-0 left-0 w-full h-[35px] bg-[#262626] flex items-center justify-center z-10">{{ item.title }}</p>
            </li>
        </ul>
    </div>
</template>

<script setup>
    const {subject, highlight, data} = defineProps({
        subject: { type: String },
        highlight: { type: String },
        data: Array
    })

    console.log(data)
</script>
