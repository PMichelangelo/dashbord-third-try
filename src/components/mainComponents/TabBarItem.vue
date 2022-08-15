<script setup>
import Counter from '../Counter.vue';


const props = defineProps({
  label: {
    type: String,
    required: true
  },
  icon: {
    type: String,
    required: true
  },
  count: {
    type: Number,
    default: 0
  }
})
</script>

<template>
  <a href="#" class="menu-item">
    <span class="material-icons"> <img :src=props.icon></span>
    <Counter v-if="props.count > 0" :count="props.count" class="counter" />
    <span class="menu-item-label"> {{ props.label }}</span>
  </a>
</template>

<style scoped>
.menu-item {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  min-width: 64px;
  min-height: 40px;
  border-radius: 8px;
  position: relative;
}

.menu-item:focus {
  background-color: #e8ebf8;
  border-radius: 8px;
}



.material-icons {
  color: mix(#fff, #342ead, 60%);

}

.menu-item-label {
  display: flex;
  align-items: center;
  text-align: center;
  font-weight: 400;
  font-size: 10px;
  line-height: 12px;
  color: #757D8A;
}

.menu-item-label:focus {
  color: #4E73F8;
}

.counter {
  position: absolute;
  top: 0;
  right: 0;

}
</style>