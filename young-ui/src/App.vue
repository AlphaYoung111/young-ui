<template>
  <div id="app">
    <h1>按钮组件测试</h1>
    <test-button />
    <h1>对话框组件测试</h1>
    <test-dialog />
    <h1>输入框组件测试</h1>
    <test-input />
    <h1>开关组件测试</h1>
    <test-switch />
    <h1>选择器组件测试</h1>
    <test-radio />
  </div>
</template>

<script>
import TestButton from "@/example/TestButton";
import TestDialog from "@/example/TestDialog";
import TestInput from "@/example/TestInput";
import TestSwitch from "@/example/TestSwitch";
import TestRadio from "@/example/TestRadio";
export default {
  components: {
    TestButton,
    TestDialog,
    TestInput,
    TestSwitch,
    TestRadio
  }
};
</script>

<style lang="scss">
#app{
  margin-left: 50px;
}
</style>
