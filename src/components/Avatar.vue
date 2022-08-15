<script setup>
const props = defineProps({
  icon: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div><img :src="props.icon" alt="avatar" class="avatar" /></div>
</template>

<style scooped>
.avatar {
  width: 64px;
  height: 64px;
  border-radius: 100%;
}

@media (max-width:480px) {
  .avatar {
    width: 32px;
    height: 32px;
    border-radius: 100%;
  }

}
</style>
