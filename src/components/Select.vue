<template>
  <select>
    <option v-for="option in options" :value="option.value" :key="option.value">
      {{ option.text }}
    </option>
    <slot></slot>
  </select>
</template>
<style scoped>
select {
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
<script lang="ts">
export default {
  props: {
    options: {
      type: Array<{ value: string; text: string }>,
      default: () => [],
    },
  },
};
</script>
