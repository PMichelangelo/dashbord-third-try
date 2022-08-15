<script setup>
const props = defineProps({
  complete: {
    type: Boolean,
    required: false,
    default: false
  }
})
</script>

<template>
  <input type="checkbox" class="checkbox">
</template>

<style scoped>
.checkbox {
  padding: 0;
  margin: 0;
}
</style>