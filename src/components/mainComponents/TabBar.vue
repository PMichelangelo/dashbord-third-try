<script setup>


import iconData from "../../assets/icons/menu.svg";
import TabBarItem from "./TabBarItem.vue";

const tabbar = [
  {
    label: "Table",
    icon: iconData
  },
  {
    label: "Home",
    icon: iconData
  },
  {
    label: "Sales",
    icon: iconData,
    count: 8,
  },
  {
    label: "Project",
    icon: iconData
  },
  {
    label: "Encommerce",
    icon: iconData
  },
]
</script>

<template>
  <div class="container">
    <nav class="menu">
      <TabBarItem v-for="item in tabbar" v-bind="item"></TabBarItem>
    </nav>
  </div>
</template>

<style scoped>
.contaier {
  display: none;
}

.menu {
  display: none;
}

@media (max-width:480px) {
  .container {
    height: 48px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #f7f5f8;
    padding: 4px;
  }


  .menu {
    display: flex;
    width: 100%;
    justify-content: space-between;
    overflow: hidden;
  }
}
</style>