<script setup>
import Header from "./Header.vue";
import Divider from "../Divider.vue";
import ButtonSetings from "../ButtonSetings.vue";

import settingsAltIcon from "../../assets/icons/settings-alt.svg"
import Button from "../Button.vue";
import Spacing from "../Spacing.vue";
import MetricCardMini from "./MetricCardMini.vue";

import TableMain from "./TableMain.vue";
import ButtonMobile from "./ButtonMobile.vue";

import Checkbox from "./Checkbox.vue";
import TabBar from "./TabBar.vue";
import BackgroundSeparator from "./BackgroundSeparator.vue";

const cards = [
  {
    label: "Total budget",
    price: "$74,994.00"
  },
  {
    label: "Monthly Budget",
    price: "$12,315.89",
    down: true,
  },
  {
    label: "Weekly Budget",
    price: "$3,476.15",

  },
  {
    label: "Today Budget",
    price: "$777.00",
    down: true,
  },

]
</script>

<template>
  <Header />
  <Divider />
  <div class="main-wrapper">
    <div class="label-wrapper">
      <h2>Employees</h2>
      <p class="p-hiden"> Subcaption</p>
      <p class="p-phone-hiden">18 result found</p>
    </div>
    <Spacing />
    <div class="buttons-wrapper">
      <ButtonSetings :icon="settingsAltIcon" />
      <Button>
        <img src="../../assets/icons/sort.svg" alt="sort">
        <p>Sort:<b> Chronological</b></p>
      </Button>
      <Button>
        <div class="inner">
          <span class="icon"> <img src="../../assets/icons/right-arrow.svg" alt=""
              style="transform:rotate(180deg)"></span>
          <span class="label"> <b>August,</b> 2021</span>
          <span class="icon"><img src="../../assets/icons/right-arrow.svg" alt=""></span>
        </div>
      </Button>
    </div>
    <Button class="btn-mobile">
      <span class="icon"> <img src="../../assets/icons/filter.svg" alt="filter" style="transform:scaleX(-1) ;"></span>
      <span class="label-mobile"> Filters</span>
    </Button>
  </div>
  <div class="main-wrapper">
    <MetricCardMini v-for="item in cards" v-bind="item"></MetricCardMini>
  </div>
  <div class="search-results">
    <p class="p-hiden">18 result found</p>
    <Spacing />
    <ButtonMobile damage>
      <span><img src="../../assets/icons/trash.svg" alt="trash"></span>
      <span><b>Delete</b></span>
    </ButtonMobile>
    <ButtonMobile>
      <span><img src="../../assets/icons/pencil.svg" alt="pencil" style="fill:#F43C3C ;"></span>
      <span><b>Edit</b></span>
    </ButtonMobile>
    <Checkbox />
  </div>
  <BackgroundSeparator />
  <TableMain />
  <TabBar />
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

.p-hiden {
  display: none;
}

.label {
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
  color: #757D8A;
}

.inner {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 8px;
  margin: 0 10px
}

.buttons-wrapper {
  display: flex;
  flex-direction: row;
  gap: 24px;
}

.btn-mobile {
  display: none;
}

.search-results {
  display: none;
}

@media (max-width:480px) {

  h2 {
    font-weight: 700;
    font-size: 16px;
    line-height: 24px;
  }

  .p-phone-hiden {
    display: none;
  }

  .p-hiden {
    display: flex;
    font-weight: 400;
    font-size: 14px;
    line-height: 20px;
  }

  .inner {
    display: none;
  }

  .buttons-wrapper {
    display: none;
  }

  .label-mobile {
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    color: #5A6474;
  }

  .btn-mobile {
    display: flex;
    border: 1px solid #E1E3E6;
    max-height: 40px;
    gap: 8px;
  }

  .main-wrapper {
    overflow: scroll;
    padding: 16px 16px 0 16px;
    gap: 8px;
    justify-content: flex-start;
  }

  .main-wrapper::-webkit-scrollbar {
    display: none;
  }

  .label-wrapper {
    gap: 0;
  }


  .search-results {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 16px 16px 8px 16px;
    gap: 12px;
  }
}
</style>