<script setup>
import { STATUSES_NAME, STATUS_VACANTION } from './statuses';

const props = defineProps({
  row: {
    type: Object,
    required: true,
  },
});


</script>

<template>
  <p :class="`status${row.status_id}`">{{ STATUSES_NAME[row.status_id] }}</p>
  <p v-if="row.status_id === STATUS_VACANTION" class="vacantion">Until the next week</p>

</template>

<style scooped>
.status0 {
  color: #4E73F8;
}

.status1 {
  color: #F43C3C;
}

.status2 {
  color: #757D8A;
}

.status3 {
  color: #FCA549;
}

.vacantion {
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
}
</style>

