<script setup>
import Header from "./Header.vue";
import Divider from "../Divider.vue";
import ButtonSetings from "../ButtonSetings.vue";

import settingsAltIcon from "../../assets/icons/settings-alt.svg"
import Button from "../Button.vue";
import Spacing from "../Spacing.vue";
import MetricCardMini from "./MetricCardMini.vue";

import TableMain from "./TableMain.vue";

const cards = [
    {
        label: "Total budget",
        price: "$74,994.00"
    },
    {
        label: "Monthly Budget",
        price: "$12,315.89"
    },
    {
        label: "Weekly Budget",
        price: "$3,476.15",
        down: true,
    },
    {
        label: "Today Budget",
        price: "$777.00"
    },

]
</script>

<template>
    <Header />
    <Divider />
    <div class="main-wrapper">
        <div>
            <h2>Employees</h2>
            <p>18 result found</p>
        </div>
        <Spacing />
        <ButtonSetings :icon="settingsAltIcon" />
        <Button>
            <img src="../../assets/icons/sort.svg" alt="sort">
            <p>Sort:<b> Chronological</b></p>
        </Button>
        <Button>
            <p> &#10094; <b>August, </b> 2021
                &#10095;</p>
        </Button>
    </div>
    <div class="main-wrapper">
        <MetricCardMini v-for="item in cards" v-bind="item"></MetricCardMini>
    </div>
    <TableMain />

</template>

<style scoped>
.main-wrapper {
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
    gap: 24px;
    padding: 24px;
}

div {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 0px;
    gap: 8px;
}

h2 {
    color: #404D61;
}

p {
    font-weight: 400;
    font-size: 18px;
    line-height: 24px;
    color: #757D8A;
}
</style>