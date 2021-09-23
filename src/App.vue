<template>
<!-- 若是屏幕的最小值小于1280px则使用max-w-5xl否则使用3xl -->
<div class="max-w-3xl px-4 mx-auto md:px-6 xl:max-w-5xl xl:px-0">
    <Nav />
    <Search />
    <router-view></router-view>
    <Footer />
    <!-- <FootNav /> -->
</div>

</template>

<script setup>
import Nav from './components/Nav.vue';
import Footer from './components/Foot.vue'
import Search from './components/propscomponent/Search.vue'
import FootNav from './components/FootNav.vue'

</script>

<style>

</style>
