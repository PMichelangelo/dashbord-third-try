<script setup>
import Sidebar from './Sidebar.vue';
import Main from './mainComponents/Main.vue';

</script>

<template>
    <div class="app">
        <Sidebar />
        <div class="main">
            <Main />
        </div>
    </div>

</template>

<style scoped>
.app {
    display: flex;
    flex-direction: row;
    width: 100%;
}

.main {
    width: 100%;
}
</style>

