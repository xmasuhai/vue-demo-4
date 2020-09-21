<template>
<div v-if="show">
  <p>默认初始值是{{show}}，所以是显示的</p>
  <button @click.stop="closeDiv">关闭</button>
</div>
</template>

<script>
export default {
  name: "myComponent",
  props: ["show"],
  methods: {
    closeDiv() {
      this.$emit("update:show", false);
    },
  },
};
</script>

<style scoped>
</style>
