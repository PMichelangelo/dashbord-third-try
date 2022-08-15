<template>
  <div class="wrapper-buttons">
    <button class="action-button"> <img src="../../assets/icons/pencil.svg" alt=""></button>
    <button class="action-button"> <img src="../../assets/icons/trash.svg" alt=""></button>
  </div>

</template>


<style >
.wrapper-buttons {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  opacity: 0;
  gap: 16px;
  padding-right: 16px;
}

.action-button {
  border: none;
  background-color: transparent;
  box-shadow: none;
  padding: 0;
}

tr:hover .wrapper-buttons {
  opacity: 1;
}
</style>