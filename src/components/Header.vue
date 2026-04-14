<template>
    <header class="header">
        <div class="container h-20 px-[1.875rem] max-w-screen flex justify-start items-center">
            <div class="header__logo">
                <router-link to="/">
                    <img src="@/assets/images/logo.png" alt="">
                </router-link>
            </div>
            <nav class="header__nav ml-auto">
                <ul class="header__nav-list flex items-center text-base">
                    <li class="header__nav-item pr-[.625rem]">
                        <router-link to="/" active-class="text-[#2E83C5]">홈</router-link>
                    </li>
                    <li class="header__nav-item pr-[.625rem]">
                        <router-link to="/match" active-class="text-[#2E83C5]">전적검색</router-link>
                    </li>
                </ul>
            </nav>
            <div class="header__auth">
                <BaseButton>디스코드 로그인</BaseButton>
            </div>
        </div>
    </header>
</template>

<script setup>
    import BaseButton from './BaseButton.vue'
</script>