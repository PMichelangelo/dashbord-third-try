<script setup>

import TableItem from "./TableItem.vue"
import tableIcon from "../../assets/icons/tableIcon.png"


const table = [
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
                <th>Name <img src="" alt=""></th>
                <th>Email <img src="../../assets/icons/up-arrow.svg" alt=""></th>
                <th>Status <img src="" alt=""></th>
                <th>Role <img src="" alt=""></th>
            </tr>
        </thead>
        <tbody>
            <TableItem v-for="item in table" v-bind="item"></TableItem>
        </tbody>
    </table>
</template>

<style scoped>
table {
    display: flex;
    justify-content: space-between;
    align-items: center;
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
</style>