<script setup>
const props = defineProps({
  row: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <p v-bind="name in row">
    {{ row.name }} </p>
</template>
