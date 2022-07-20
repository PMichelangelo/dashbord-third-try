<script setup>
import Counter from "./Counter.vue";
import Spacing from "./Spacing.vue";
import IconDraggable from "./IconDraggable.vue";

const props = defineProps({
  label: {
    type: String,
    required: true,
  },
  count: {
    type: Number,
    default: 0,
  },
  draggable: {
    type: Boolean,
    default: false,
  },
  icon: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <li>
    <img :src="props.icon" />
    <span>{{ props.label }}</span>
    <Spacing />
    <Counter v-if="props.count > 0" :count="props.count" class="counter" />
    <IconDraggable v-if="props.draggable" />
  </li>
</template>

<style scoped>
li {
  display: flex;
}

.counter {
  margin-right: 12px;
}
</style>
