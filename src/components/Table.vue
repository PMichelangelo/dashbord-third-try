<script setup>
import Sidebar from './Sidebar.vue';
import Main from './mainComponents/Main.vue';

</script>

<template>
    <div class="app">
        <Sidebar />
        <div class="wrapper">
            <Main />
        </div>
    </div>

</template>

<style scoped>
.app {
    display: flex;
    flex-direction: row;
}
</style>

