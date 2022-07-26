<script setup>
import AccountItem from "./AccountItem.vue";
import SidebarItem from "./SidebarItem.vue";
import Spacing from "./Spacing.vue";

import iconCalendar from "../assets/icons/calendar.svg";
import iconData from "../assets/icons/menu.svg";
import iconKanban from "../assets/icons/kanban.svg";
import iconMessenger from "../assets/icons/messenger.svg";
import iconAnalytics from "../assets/icons/diagram.svg";
import iconCrypto from "../assets/icons/pulse-rate.svg";
import iconLogOut from "../assets/icons/logout.svg"

const menu = [
  {
    label: "Data table",
    icon: iconData,
  },
  {
    label: "Kanban",
    icon: iconKanban,
  },
  {
    label: "Analytics",
    icon: iconAnalytics,
    count: 14,
  },
  {
    label: "Calendar",
    icon: iconCalendar,
  },
  {
    label: "Messenger",
    icon: iconMessenger,
  },
  {
    label: "Crypto",
    icon: iconCrypto,
  },
];
</script>

<template>
  <aside>
    <header>
      <AccountItem />
    </header>
    <main>
      <ul>
        <li>
          <img src="../assets/icons/free-icon-search-149852.svg" alt="search"> <input type="text"
            placeholder="Search" />
        </li>
        <SidebarItem v-for="item in menu" v-bind="item" draggable />
      </ul>
    </main>
    <Spacing />
    <footer>
      <ul>
        <SidebarItem label="Support" :icon="iconMessenger" />
        <SidebarItem label="Sign Out" :icon="iconLogOut" />
      </ul>
    </footer>
  </aside>
</template>

<style>
aside {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 378px;
  height: 100%;
  background: #f8f8f8;
  opacity: 0.97;
  padding: 32px 24px;
  align-self: stretch;

}

main {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 0px;
  margin-top: 40px;
  gap: 16px;
  width: 330px;
}

input {
  width: 218px;
  height: 24px;
  width: 218px;
  height: 24px;
  border: none;
  display: flex;
  align-items: center;
  color: #757d8a;
  background: transparent;
}

li {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: stretch;
  width: 330px;
  color: #757d8a;
  height: 48px;
}

li>img {
  margin: 0 19px;
}

footer {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 0px;
  color: #757d8a;
}

footer>p {
  display: flex;
  flex-direction: row;
  align-items: center;

  width: 330px;
  height: 48px;
}

footer>p>img {
  margin: 0 19px;
}
</style>
