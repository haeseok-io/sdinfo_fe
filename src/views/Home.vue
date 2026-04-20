<template>
    <main>
        <section class="flex items-center justify-center bg-[url(/src/assets/images/home_bg01.png)] bg-cover min-h-[500px]">
            <form action="">
                <p class="text-[#B2B2C2] mb-[10px]">서든어택 전적검색 및 매치 분석 플랫폼</p>
                <label for="search" class="relative">
                    <input type="text" id="search" name="search" placeholder="유저 닉네임을 입력해주세요." class="w-[700px] h-[50px] bg-[#262626] border border-[#B2B2C2] focus:border-[#2E83C5] rounded-md outline-none px-4 placeholder-[#666] text-[#B2B2C2]">
                    <button type="submit" class="absolute right-4 top-1/2 -translate-y-1/2 text-xs text-[#B2B2C2]">
                        <Search />
                    </button>
                </label>
            </form>
        </section>
        <div class="container">
            <section class="mt-25">
                <RankMapList highlight="5vs5 랭크전" subject="2026 시즌1" :data="maps"/>
                <RankMapList class="mt-25" highlight="3vs3 랭크전" subject="2026 시즌1" :data="maps"/>
            </section>
            <section class="mt-25 flex gap-5">
                <BoardShort class="flex-1" highlight="서든어택" subject="공지사항" :data="saNoticeData" />
                <BoardShort class="flex-1" highlight="SuddenInfo" subject="공지사항" :data="siNoticeData" />
            </section>
        </div>
    </main>
</template>

<script setup>
    import { Search } from 'lucide-vue-next'
    import RankMapList from '@/components/RankMapList.vue'
    import BoardShort from '../components/BoardShort.vue'

    // 테스트용 json
    import maps from '@/assets/mapTest.json'
    import notices from '@/assets/boardTest.json'

    const saNoticeData = notices.filter(item => item.type===1)
    const siNoticeData = notices.filter(item => item.type===2)
</script>