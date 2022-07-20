<script setup>
import Avatar from "./Avatar.vue";
import Counter from "./Counter.vue";
import Button from "./Button.vue";
import Spacing from "./Spacing.vue";
</script>

<template>
  <div class="account">
    <Avatar />
    <div>
      <p class="p-label">Welcom back,</p>
      <h2>Sweet Girl</h2>
    </div>
    <Spacing />
    <Counter count="101" danger />
    <button>
      <img src="./icons/settings.svg" alt="settings" />
    </button>
  </div>
</template>

<style>
.account {
  display: flex;
  flex-direction: row;

  height: 66px;
  gap: 12px;
  align-items: center;
}

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
}

.p-label {
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
  color: #757d8a;
}
</style>
