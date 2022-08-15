<script setup>
const props = defineProps({
  damage: {
    type: Boolean,
    required: false,
    default: false
  }
})
</script>

<template>

  <button :class="{ damage }">
    <slot />
  </button>

</template>

<style scoped>
button {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 6px;
  box-shadow: 0px 4px 2px -2px rgba(27, 46, 94, 0.02);
  border-radius: 8px;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #4E73F8;
  padding: 0;
}

button.damage {
  color: #F43C3C;
  gap: 4px;
}
</style>