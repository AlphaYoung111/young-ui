<template>
  <!-- 按钮示范 -->
  <div class="btn-example">
    <y-button>按钮</y-button>
    <y-button type="primary">按钮</y-button>
    <y-button type="danger">按钮</y-button>
    <y-button type="success">按钮</y-button>
    <y-button type="warning">按钮</y-button>
    <y-button type="info">按钮</y-button>
    <hr />
    <y-button>按钮</y-button>
    <y-button plain type="primary">按钮</y-button>
    <y-button plain type="danger">按钮</y-button>
    <y-button plain type="success">按钮</y-button>
    <y-button plain type="warning">按钮</y-button>
    <y-button plain type="info">按钮</y-button>
    <hr />
    <y-button round>按钮</y-button>
    <y-button round plain type="primary">按钮</y-button>
    <y-button round plain type="danger">按钮</y-button>
    <y-button round plain type="success">按钮</y-button>
    <y-button round plain type="warning">按钮</y-button>
    <y-button round plain type="info">按钮</y-button>
    <hr />
    <y-button circle>按</y-button>
    <y-button circle plain type="primary">按</y-button>
    <y-button circle plain type="danger">按</y-button>
    <y-button circle plain type="success">按</y-button>
    <y-button circle plain type="warning">按</y-button>
    <y-button circle plain type="info">按</y-button>
    <hr />
    <y-button icon="el-icon-delete" circle></y-button>
    <y-button icon="el-icon-delete" circle plain type="primary"></y-button>
    <y-button icon="el-icon-delete" circle plain type="danger"></y-button>
    <y-button icon="el-icon-delete" circle plain type="success"></y-button>
    <y-button icon="el-icon-delete" circle plain type="warning"></y-button>
    <y-button icon="el-icon-delete" circle plain type="info"></y-button>
  </div>
</template>
<script>
import YButton from "@/components/button/YButton";
export default {
  components: {
    YButton
  }
};
</script>
<style lang="scss" scoped>
.btn-example {
  margin: 0 auto;
  .y-button {
    margin-right: 20px;
  }
}
</style>