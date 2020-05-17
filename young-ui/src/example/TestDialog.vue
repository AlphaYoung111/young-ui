<template>
  <div>
    <button @click="visible=true">显示</button>
    <!-- <y-dialog title="温馨提示" :visible="visible"></y-dialog> -->
    <y-dialog :visible.sync="visible">
      <template #title>
        <h4>我是标题</h4>
      </template>
    </y-dialog>
  </div>
</template>
<script>
import YDialog from "@/components/dialog/YDialog";
export default {
  components: {
    YDialog
  },
  data() {
    return {
      visible: false
    };
  },
  methods: {
    closeDialog(value) {
      this.visible = value;
    }
  }
};
</script>