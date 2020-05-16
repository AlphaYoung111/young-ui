<template>
  <div id="app">
    <h1>按钮组件测试</h1>
    <test-button />
  </div>
</template>

<script>
import TestButton from "@/example/TestButton";
export default {
  components: {
    TestButton
  }
};
</script>

<style lang="scss">
#app{
  margin-left: 50px;
}
</style>
