<script setup>
import tableIcon from "../../assets/icons/tableIcon.png"

const columns = ['name', 'email', 'status', 'role']

const rows = [
  {
    name: "Roman Belic",
    email: "purchaseuikits@setproduct.com",
    status: "Free",
    role: "Art Director 😎"
  },
  {

    name: "Sarah Smith",
    email: "sk8er@palacecrew.net",
    status: "Busy",
    role: "UX Writer"
  },
  {

    name: "Eleanor Pena",
    email: "lookatmyhat@mail.me",
    status: "Working",
    role: "UX Engineer"
  },
  {

    name: "Rachel Richards",
    email: "rondondon@nfs.org",
    status: "Free",
    role: "UI Master"
  },
  {

    name: "Arlene McCoy",
    email: "arlenemccoyindagame@heyhey.com",
    status: "Working",
    role: "Product Manager"
  },
  {
    name: "Courtney Henry",
    email: "henry96@mail.com",
    status: "Free",
    role: "HR Assistant"
  },
  {

    name: "Guy Hawkins",
    email: "thatguy@fromalaska.us",
    status: "Busy",
    role: "The Boss"
  },
  {

    name: "Devon Lane",
    email: "devon_dfq@eyefind.info",
    status: "Free",
    role: "Full-Stack Developer"
  },
  {

    name: "Eleanor P. Junior",
    email: "epj2022@mail.com",
    status: "Working",
    role: "UX Engineer"
  },
  {

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
          <span class="icon-wrapper">
            <span class="icon"><img src="../../assets/icons/up-arrow.svg" alt=""></span>
          </span>
        </th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="row in rows">
        <td v-for="(value, field) in row">{{ value }} </td>
        <div class="btn-wrapper">
          <button>
            <img src="../../assets/icons/pencil.svg" alt="edit">
          </button>
          <button>
            <img src="../../assets/icons/trash.svg" alt="delete">
          </button>
        </div>
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
  padding: 24px;
  text-transform: uppercase;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #5A6474;
  text-align: left;
}

tbody tr:nth-child(odd) {
  background: #F8F8F8;
}

tbody tr:nth-child(even) {
  background: #FFFFFF;
}

td {
  padding: 18px 22px;
  gap: 16px;
  color: #5A6474;
}

td:nth-child(1) {
  font-weight: 500;
  font-size: 18px;
  line-height: 24px;
  color: #5A6474;
}

.icon {
  margin-left: 8px;
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
</style>