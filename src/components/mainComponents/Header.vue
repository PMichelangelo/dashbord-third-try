<script setup>
import Button from '../Button.vue';
import ButtonSetings from '../ButtonSetings.vue';
import pencilIcon from '../../assets/icons/pencil.svg'

import searchIcon from '../../assets/icons/free-icon-search-149852.svg';
import Spacing from '../Spacing.vue';
import Avatar from '../Avatar.vue';
import avatarIcon from '../../assets/icons/unnamed.jpg'
import settingsIcon from '../../assets/icons/settings.svg'
import emailIcon from '../../assets/icons/email.svg'
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

  <div class="header-mobile">
    <Avatar :icon="avatarIcon" />
    <Button>
      <div class="inner">
        <span class="icon"> <img src="../../assets/icons/right-arrow.svg" alt=""
            style="transform:rotate(180deg);width: 12px;  fill:#4E73F8"></span>
        <span class="label"> <b>August,</b> 2021</span>
        <span class="icon"><img src="../../assets/icons/right-arrow.svg" alt=""
            style="width: 12px;  fill:#4E73F8"></span>
      </div>
    </Button>
    <div class="btn-settings-mobile">
      <ButtonSetings :icon="emailIcon" />
      <ButtonSetings :icon="settingsIcon" />
    </div>

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
  gap: 24px;
}

img {
  width: 30px;
  height: 30px;
  vertical-align: unset;
}

.input-wrapper {
  min-width: 400px;
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
  width: 100%;
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

.header-mobile {
  display: none;
}

input:focus {
  outline: none;
  box-shadow: 0px 0px 0px 4px rgba(78, 115, 248, 0.2);
}

.account-item {
  display: none;
}

@media (max-width:480px) {
  .header {
    display: none;

  }

  .input-wrapper,
  h1 {
    display: none;
  }


  .header-mobile {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 48px;
    width: 100%;
    padding: 8px 12px;
    background-color: #f2f9fe;
    gap: 18px
  }

  .btn-settings-mobile {
    display: flex;
    flex-direction: row;
    gap: 16px;
  }

  .inner {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 8px;
    margin: 0 10px
  }

  .label {
    font-weight: 400;
    font-size: 18px;
    line-height: 24px;
    color: #757D8A;
    white-space: nowrap;
  }



}
</style>