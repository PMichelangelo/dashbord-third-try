<script setup>
import tableIcon from "../../assets/icons/tableIcon.png";
import avatarIcon from "../../assets/icons/unnamed.jpg"

const props = defineProps({
  row: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="user_wrapper">
    <img :src="tableIcon" alt="" class="user_avatar">
    <p v-bind="name in row">
      {{ row.name }} </p>
  </div>

</template>

<style scooped>
.user_wrapper {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 16px;
}

.user_avatar {
  height: 32px;
  width: 32px;
  border-radius: 99px;
}
</style>