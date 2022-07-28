<script setup>
const props = defineProps({
  row: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <p>{{ props.row }}</p>
</template>
