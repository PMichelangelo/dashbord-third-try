<script setup>
import Avatar from "./Avatar.vue";
import Counter from "./Counter.vue";
import Spacing from "./Spacing.vue";
import avatarIcon from "../assets/icons/unnamed.jpg"
import ButtonSetings from "./ButtonSetings.vue"
import settingsIcon from "../assets/icons/settings.svg"

</script>

<template>
  <div class="account">
    <Avatar :icon="avatarIcon" />
    <div>
      <p class="p-label">Welcom back,</p>
      <h2>Sweet Girl</h2>
    </div>
    <Spacing />
    <Counter count="101" danger />
    <ButtonSetings :icon="settingsIcon" />
  </div>
</template>

<style>
.account {
  display: flex;
  flex-direction: row;

  height: 66px;
  gap: 12px;
  align-items: center;
}

.p-label {
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
  color: #757d8a;
}
</style>
