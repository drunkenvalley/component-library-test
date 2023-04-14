<template>
  <select>
    <option v-for="option in options" :value="option.value" :key="option.value">
      {{ option.text }}
    </option>
    <slot></slot>
  </select>
</template>
<script>
export default {
  props: {
    options: {
      type: Array,
      default: () => [],
    },
  },
};
</script>
