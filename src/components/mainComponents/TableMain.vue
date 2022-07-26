<script setup>
import tableIcon from "../../assets/icons/tableIcon.png"

const columns = ['name', 'email', 'status', 'role']

const rows = [
  {
    icon: tableIcon,
    name: "Roman Belic",
    email: "purchaseuikits@setproduct.com",
    status: "Free",
    role: "Art Director 😎"
  },
  {
    icon: tableIcon,
    name: "Sarah Smith",
    email: "sk8er@palacecrew.net",
    status: "Busy",
    role: "UX Writer"
  },
  {
    icon: tableIcon,
    name: "Eleanor Pena",
    email: "lookatmyhat@mail.me",
    status: "Working",
    role: "UX Engineer"
  },
  {
    icon: tableIcon,
    name: "Rachel Richards",
    email: "rondondon@nfs.org",
    status: "Free",
    role: "UI Master"
  },
  {
    icon: tableIcon,
    name: "Arlene McCoy",
    email: "arlenemccoyindagame@heyhey.com",
    status: "Working",
    role: "Product Manager"
  },
  {
    icon: tableIcon,
    name: "Courtney Henry",
    email: "henry96@mail.com",
    status: "Free",
    role: "HR Assistant"
  },
  {
    icon: tableIcon,
    name: "Guy Hawkins",
    email: "thatguy@fromalaska.us",
    status: "Busy",
    role: "The Boss"
  },
  {
    icon: tableIcon,
    name: "Devon Lane",
    email: "devon_dfq@eyefind.info",
    status: "Free",
    role: "Full-Stack Developer"
  },
  {
    icon: tableIcon,
    name: "Eleanor P. Junior",
    email: "epj2022@mail.com",
    status: "Working",
    role: "UX Engineer"
  },
  {
    icon: tableIcon,
    name: "Maria Bruno",
    email: "bruno987@cast.co",
    status: "Busy",
    role: "Manager"
  },
]
</script>


<template>
  <table>
    <thead>
      <tr>
        <th v-for="column in columns">
          <span class="label">{{ column }}</span>
          <span class="icon">1</span>
        </th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="row in rows">
        <td v-for="(value, field) in row">{{ value }}</td>
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

  text-transform: uppercase;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #5A6474;
}

tbody tr:nth-child(odd) {
  background: #F8F8F8;
}

tbody tr:nth-child(even) {
  background: #FFFFFF;
}

td {
  padding: 20px 24px;
  gap: 16px;
  color: #5A6474;
}

td:nth-child(1) {
  font-weight: 500;
  font-size: 18px;
  line-height: 24px;
  color: #5A6474;
}
</style>