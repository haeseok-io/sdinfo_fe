<template>
    <main>
        <section class="hero flex items-center justify-center bg-[url(/src/assets/images/home_bg01.png)] bg-cover min-h-[500px]">
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
            리스트2
        </div>
    </main>
</template>

<script setup>
    import { Search } from 'lucide-vue-next'
</script>