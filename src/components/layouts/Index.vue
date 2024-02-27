<template>
    <el-container class="min-h-screen">
        <!-- <el-aside width="200px" class="min-h-screen">
            <Aside :isCollapse="isCollapse" />
        </el-aside> -->
        <!-- <el-container> -->
            <el-header class="flex items-center w-screen">
                <Header/>
            </el-header>
            <el-main>
                <img alt="Vue logo" class="logo" src="/favicon.ico" width="125" height="125" />
                <div class="wrapper">
                    <HelloWorld msg="开发工具箱" />
                    <nav>
                        <RouterLink to="/">Home</RouterLink>
                        <RouterLink to="/about">About</RouterLink>
                    </nav>
                </div>
            </el-main>
        <!-- </el-container> -->
    </el-container>
</template>

<script setup lang="ts">
import HelloWorld from '../HelloWorld.vue'
import Aside from './Aside.vue'
import Header from './Header.vue'

import { ref, watch } from 'vue'

const isCollapse = ref(false);
const handleIsCollapseChange = (newVal) => {
    isCollapse.value = !newVal
}

</script>


<style scoped>
.el-aside {
    width: auto !important;
}

.el-icon{
    font-size: 1.2rem !important;
}
</style>
