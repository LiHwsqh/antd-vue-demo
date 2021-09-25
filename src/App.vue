<template>
  <a-select
    v-model="selected"
    mode="multiple"
    style="width: 100%"
    placeholder="Please select"
  >
    <a-select-option v-for="i in 25" :key="(i + 9).toString(36) + i">
      {{ (i + 9).toString(36) + i }}
    </a-select-option>
  </a-select>
</template>
<script>
export default {
  data() {
    return {
      selected: [],
    };
  },
  methods: {
    handleChange(value) {
      console.log(`selected ${value}`);
    },
  },
};
</script>
