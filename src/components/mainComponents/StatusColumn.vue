<script setup>
const props = defineProps({
  row: {
    type: Object,
    required: true,
  },
});
</script>

  <template>
  <p v-bind="status in row">
    {{ row.status }} </p>
</template>

