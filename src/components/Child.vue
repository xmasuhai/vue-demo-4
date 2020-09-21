<template>
<div class="child">
  {{money}}
  <button @click="$emit('update:money', money-100)">
    <span>花钱</span>
  </button>
</div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {},
  props: ["money"],
};
</script>

<style scoped>
.child {
  border: 3px solid yellowgreen;
}
</style>
