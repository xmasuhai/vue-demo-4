<template>
<div id="app" class="app">
  App.vue 我现在有{{total}}
  <hr />
  <Child :money.sync="total" />
  <!--  <Child :money.sync="total" @update:money="total = $event" />-->
  <!--  <Child :money="total" @update:money="total = $event" />-->
  <!--  <Child :money="total" v-on:update:money="total = $event" />-->
  <hr />
  <SyncMyComponent />
</div>
</template>

<script>
import Child from "./components/Child.vue";
import SyncMyComponent from "./components/SyncMyComponent.vue";

export default {
  name: "App",
  components: {
    // Child: Child,
    // 简写
    Child,
    SyncMyComponent,
  },
  data() {
    return {
      total: 10000,
    };
  },
};
</script>

<style lang="scss">
#app {
  border: 3px solid orange;
  padding: 10px;
}
</style>
