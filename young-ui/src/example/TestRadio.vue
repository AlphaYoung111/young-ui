<template>
  <div>
    <y-radio label="1" v-model="gender">男</y-radio>
    <y-radio label="0" v-model="gender">女</y-radio>
  </div>
</template>
<script>
import YRadio from "@/components/radio/YRadio";
export default {
  components: {
    YRadio
  },
  data() {
    return {
      gender: "1"
    };
  }
};
</script>