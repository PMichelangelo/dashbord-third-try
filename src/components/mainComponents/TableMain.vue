<script setup>
import tableIcon from "../../assets/icons/tableIcon.png";
import UserColumn from "./UserColumn.vue";
import StatusColumn from "./StatusColumn.vue";
import ActionColumn from "./ActionColumn.vue";
import { STATUS_FREE, STATUS_BUSY, STATUS_WORKING, STATUS_VACANTION } from './statuses.js'

const columns = [
  {
    label: "name",
    key: "name",
    component: UserColumn,
  },
  {
    label: "email",
    key: "email",
  },
  {
    label: "status",
    key: "status",
    component: StatusColumn,
  },
  {
    label: "role",
    key: "role",
  },
  {
    label: "",
    component: ActionColumn
  }
];

const rows = [
  {
    icon: tableIcon,
    name: "Roman Belic",
    email: "purchaseuikits@setproduct.com",
    status_id: STATUS_FREE,
    role: "Art Director 😎",
  },
  {
    name: "Sarah Smith",
    email: "sk8er@palacecrew.net",
    status_id: STATUS_BUSY,
    role: "UX Writer",
  },
  {
    name: "Eleanor Pena",
    email: "lookatmyhat@mail.me",
    status_id: STATUS_WORKING,
    role: "UX Engineer",
  },
  {
    name: "Rachel Richards",
    email: "rondondon@nfs.org",
    status_id: STATUS_FREE,
    role: "UI Master",
  },
  {
    name: "Arlene McCoy",
    email: "arlenemccoyindagame@heyhey.com",
    status_id: STATUS_WORKING,
    role: "Product Manager",
  },
  {
    name: "Courtney Henry",
    email: "henry96@mail.com",
    status_id: STATUS_FREE,
    role: "HR Assistant",
  },
  {
    name: "Guy Hawkins",
    email: "thatguy@fromalaska.us",
    status_id: STATUS_BUSY,
    role: "The Boss",
  },
  {
    name: "Devon Lane",
    email: "devon_dfq@eyefind.info",
    status_id: STATUS_VACANTION,
    role: "Full-Stack Developer",
  },
  {
    name: "Eleanor P. Junior",
    email: "epj2022@mail.com",
    status_id: STATUS_WORKING,
    role: "UX Engineer",
  },
  {

    name: "Maria Bruno",
    email: "bruno987@cast.co",
    status_id: STATUS_BUSY,
    role: "Manager",
  },
];
const COLUMN_KEY = "status";
</script>

<template>
  <table>
    <thead>
      <tr>
        <th v-for="column in columns">
          <span class="label">{{ column.label }}</span>
          <span class="icon-wrapper">
            <span class="icon"><img src="../../assets/icons/up-arrow.svg" alt="" /></span>
          </span>
        </th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="row_item in rows">
        <td v-for="column_item in columns">
          <p v-if="column_item.component">
            <component :is="column_item.component" :row="row_item" />
          </p>
          <p v-else>{{ row_item[column_item.key] }}</p>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped>
table {
  width: 100%;
  border-collapse: collapse;
}

thead th {
  padding: 22px 24px;
  text-transform: uppercase;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #5a6474;
  text-align: left;
  max-height: 64px;
}

th:nth-child(odd) .icon-wrapper {
  display: inline-block;
  transform: rotate(180deg);
}

tbody tr:nth-child(odd) {
  background: #f8f8f8;
}

tbody tr:nth-child(even) {
  background: #ffffff;
}

td {
  padding: 16px 24px;
  gap: 16px;
  color: #5a6474;
  max-height: 64px;
  vertical-align: middle;
  white-space: nowrap;
}

td:nth-child(1) {
  font-weight: 500;
  font-size: 18px;
  line-height: 24px;
  color: #5a6474;
  white-space: nowrap;
}

td:last-child {
  padding: 0;
}

td:nth-child(4) {
  padding-right: 0px;
}

.icon {
  display: inline-block;
  margin-left: 8px;

}

th.icon:nth-child(odd) {
  display: inline-block;
  transform: rotate(180deg);
}

.btn-wrapper {
  display: none;
}

button {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 24px;
  height: 24px;
  border: none;
  background-color: transparent;
  box-shadow: none;
}

tr:hover .btn-wrapper {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

th:last-child {
  display: none;
  max-width: 64px;
}

@media (max-width:480px) {
  table {
    display: none;
  }
}
</style>
