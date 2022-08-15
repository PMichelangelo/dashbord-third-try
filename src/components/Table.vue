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

/* smartphones, portrait iPhone, portrait 480x320 phones (Android) */
@media (max-width:320px) {}

/* smartphones, Android phones, landscape iPhone */
@media (max-width:480px) {
  aside {
    display: none;
  }

  .header {
    background-color: black;
  }
}

/* portrait tablets, portrait iPad, e-readers (Nook/Kindle), landscape 800x480 phones (Android) */
@media (min-width:600px) {}

/* tablet, landscape iPad, lo-res laptops ands desktops */
@media (min-width:801px) {
  /* tablet, landscape iPad, lo-res laptops ands desktops */
}

/* big landscape tablets, laptops, and desktops */
@media (min-width:1025px) {}

/* hi-res laptops and desktops */
@media (min-width:1281px) {}
</style>

