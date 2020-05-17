<template>
  <div>
    <y-input placeholder="请输入用户名" v-model="name"></y-input>
    <hr />
    <y-input placeholder="请输入用户名" v-model="name" clearable showPassword></y-input>
  </div>
</template>

<script>
import YInput from "@/components/input/YInput";
export default {
  components: {
    YInput
  },
  data() {
    return {
      name: ""
    };
  }
};
</script>

<style>
</style>