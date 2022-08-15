<script setup>
const props = defineProps({
  icon: {
    type: String,
    requiered: true
  }
})
</script>

<template>
  <button><img :src="props.icon"></button>
</template>

<style scoped>
button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 64px;
  height: 48px;
  border: 1px solid #e1e3e6;
  box-shadow: 0px 4px 2px -2px rgba(27, 46, 94, 0.02);
  border-radius: 8px;
  padding: 0;
  background: #FFFFFF;
}

@media (max-width:480px) {
  button {
    border: none;
    background-color: transparent;
    width: 24px;
    height: 24px;

  }
}
</style>