<script setup>

const props = defineProps({
  label: {
    type: String,
    required: true,
  },
  price: {
    type: String,
    required: true,
  },
  down: {
    type: Boolean,
    default: false
  }
})
</script>

<template>
  <div class="wrapper">
    <div class="label">
      <p>{{ props.label }}</p>
      <svg :class="{ down: props.down }" class="icon" version="1.0" xmlns="http://www.w3.org/2000/svg" width="12"
        height="12" viewBox="0 0 512 512">
        <path
          d="M247.5 113.3c-2.2.8-5.6 2.2-7.5 3.1-1.9 1-55.3 53.6-118.7 117C-8 362.5.5 353.1.5 368c.1 5.6.6 8.8 2.4 12.7 2.9 6.6 11 14.3 17.6 16.9 4.9 1.9 10.3 1.9 235.5 1.9s230.6 0 235.5-1.9c6.6-2.6 14.7-10.3 17.6-16.9 1.8-3.9 2.3-7.1 2.4-12.7 0-14.9 8.5-5.5-120.8-134.7C287 129.6 274.9 117.8 269.6 115.4c-6.9-3.1-16.2-4-22.1-2.1z" />
      </svg>
    </div>
    <h2> {{ props.price }}</h2>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 24px 16px;
  gap: 4px;
  height: 144px;
  width: 100%;
  background: #F8F8F8;
  border-radius: 8px;
  white-space: nowrap;
}

.icon {
  fill: green;
}

.icon.down {
  transform: rotate(180deg);
  fill: red;
}

.label {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0px;
  gap: 10px;
  height: 24px;
}

p {
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
  color: #757D8A;
}

h2 {
  font-weight: 700;
  font-size: 24px;
  line-height: 32px;
  color: #404D61;
}

.wrapper:hover {
  background: linear-gradient(180deg, #6989FE 0%, #3C64F4 100%);

}

.wrapper:hover h2 {
  color: white;
}

.wrapper:hover p {
  color: white;
}

.wrapper:hover .icon {
  fill: #F8F8F8;
}
</style>