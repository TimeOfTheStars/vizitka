<template>
    <div class="layout">
        <TheHeader />
        <main class="main" :class="{ 'main--with-offset': !isHomePage }">
            <slot />
        </main>
        <TheFooter />
    </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const isHomePage = computed(() => route.path === '/')
</script>

<style scoped>
.layout {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}
.main {
    flex: 1;
    padding-top: 0;
}
.main.main--with-offset {
    padding-top: 120px;
}
</style>
