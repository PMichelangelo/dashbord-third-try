<script setup>
import tableIcon from "../../assets/icons/tableIcon.png";


const props = defineProps({
  row: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="user_wrapper">
    <img :src="row.icon" alt="" class="user_avatar">
    <p>{{ row.name }} </p>
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