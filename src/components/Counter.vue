<script setup>
import { computed } from "@vue/reactivity";

const props = defineProps({
  count: {
    type: Number,
    required: true,
  },
  danger: {
    type: Boolean,
    default: false,
  },
});

const formatedCount = computed(() =>
  props.count >= 100 ? "99+" : props.count
);
</script>

<template>
  <div :class="{ danger: props.danger }">{{ formatedCount }}</div>
</template>

<style scoped>
.danger {
  background: linear-gradient(180deg, #ff5959 0%, #ef2c2c 100%);
}

div {
  display: flex;
  flex-direction: row;
  height: 24px;
  align-items: center;
  justify-content: center;
  background: linear-gradient(180deg, #6989fe 0%, #3c64f4 100%);
  border-radius: 99px;
  color: #fff;
  font-weight: 700;
  font-size: 14px;
  line-height: 20px;
  padding: 0 7.5px;
}

@media (max-width:480px) {
  div {
    width: 14px;
    height: 14px;
  }
}
</style>
