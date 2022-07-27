<script setup>
import Button from '../Button.vue';
import ButtonSetings from '../ButtonSetings.vue';
import pencilIcon from '../../assets/icons/pencil.svg'

import searchIcon from '../../assets/icons/free-icon-search-149852.svg';
import Spacing from '../Spacing.vue';
</script>

<template>
  <div class="header">
    <h1> Data Table <img src="../../assets/icons/clipboard_1f4cb.png" alt="clipboard"></h1>
    <Spacing />
    <div class="input-wrapper">
      <img :src="searchIcon" alt="" class="input-icon">
      <input type="search" placeholder="Search">
    </div>
    <Spacing />
    <Button primary> Add persone</Button>
    <ButtonSetings :icon="pencilIcon" />
  </div>
</template>

<style scoped>
.header {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  height: 96px;
  padding: 24px;
}

img {
  width: 30px;
  height: 30px;
  vertical-align: unset;
}

.input-wrapper {
  position: relative;
}

.input-icon {
  width: 20px;
  position: absolute;
  top: 50%;
  left: 16px;
  transform: translate(0, -50%);
}

input {
  display: flex;
  align-items: center;
  height: 48px;
  width: 459px;
  border: 1px solid #4E73F8;
  border-radius: 8px;

  text-indent: 48px;
  color: #5A6474;
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
}

input::-webkit-search-cancel-button {
  -webkit-appearance: none;
  height: 24px;
  width: 24px;
  background-color: #F1F2F3;
  background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='%23777'><path d='M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12z'/></svg>");
  cursor: pointer;
  position: relative;
  right: 16px;
  border-radius: 99px;
  border: none;
}

.clear {

  padding: 6px;
  min-width: 24px;
  max-height: 24px;
  border-radius: 100%;
  border: none;
  color: #757D8A;
  background-color: #F1F2F3;
  position: relative;
  right: 16px;


}

input:focus {
  outline: none;
  box-shadow: 0px 0px 0px 4px rgba(78, 115, 248, 0.2);
}
</style>