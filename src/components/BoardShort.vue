<template>
    <div class="boardShort">
        <h2 class="mb-5 flex items-center justify-between">
            <p class="font-bold text-2xl"><span class="text-[#2E83C5]">{{ highlight }}</span> {{ subject }}</p>
            <a :href="`${moreLink}`" class="text-[#B2B2C2]">더보기</a>
        </h2>
        <ul class="bg-[#262626] border border-[#3C3C3C] rounded-xl p-4">
            <li v-for="item in data" :key="item.id" class="flex items-center justify-between mb-2.5 last:mb-0">
                <p>{{ item.subject }}</p>
                <p>{{ item.date }}</p>
            </li>
        </ul>
    </div>
</template>

<script setup>
    const { subject, highlight, moreLink, data } = defineProps({
        subject: { type: String },
        highlight: { type: String },
        moreLink: { type: String, default: "#" },
        data: { type: Array }
    })
</script>