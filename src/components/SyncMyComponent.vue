<template>
<div class="details">
  <br />
  <p>父组件</p>
  <button @click="changeValue">toggle</button>
  <MyComponent :show.sync="valueChild" class="myComponent" />
</div>
</template>

<script>
import MyComponent from "./MyComponent";
export default {
  components: {
    MyComponent,
  },
  data() {
    return {
      valueChild: true,
    };
  },
  methods: {
    changeValue() {
      this.valueChild = !this.valueChild;
    },
  },
};
</script>

<style lang="scss" scoped>
.myComponent {
  padding: 30px 20px 30px 5px;
  border: 1px solid #ddd;
  margin-bottom: 10px;
}
</style>
