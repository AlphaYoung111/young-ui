<template>
  <div class="hm-switch" @click="handleChange" :class="{ 'is-checked': this.value }">
    <input class="hm-switch__input" type="checkbox" ref="input" :name="name" />
    <span class="hm-switch__core" ref="core">
      <span class="hm-switch__button"></span>
    </span>
  </div>
</template>
<script>
export default {
  props: {
    value: {
      type: Boolean,
      default: false
    },
    name: {
      type: String,
      default: ""
    },
    activeColor: {
      type: String,
      default: ""
    },
    inactiveColor: {
      type: String,
      default: ""
    }
  },
  mounted() {
    this.$refs.input.checked = this.value;
    this.setBackgroundColor();
  },
  methods: {
    async handleChange() {
      this.$emit("input", !this.value);
      await this.$nextTick();
      this.$refs.input.checked = this.value;
    },
    setBackgroundColor() {
      if (this.activeColor || this.inactiveColor) {
        let color = this.value ? this.activeColor : this.inactiveColor;
        this.$refs.core.style.borderColor = color;
        this.$refs.core.style.backgroundColor = color;
      }
    }
  },
  watch: {
    value() {
      this.setBackgroundColor();
    }
  }
};
</script>
<style lang="scss" scoped>
.hm-switch {
  display: inline-flex;
  align-items: center;
  position: relative;
  font-size: 14px;
  line-height: 20px;
  height: 20px;
  vertical-align: middle;

  .hm-switch__input {
    position: absolute;
    width: 0;
    height: 0;
    opacity: 0;
    margin: 0;
  }
  .hm-switch__core {
    margin: 0;
    display: inline-block;
    position: relative;
    width: 40px;
    height: 20px;
    border: 1px solid #dcdfe6;
    outline: none;
    border-radius: 10px;
    box-sizing: border-box;
    background: #dcdfe6;
    cursor: pointer;
    transition: border-color 0.3s, background-color 0.3s;
    vertical-align: middle;
    .hm-switch__button {
      position: absolute;
      top: 1px;
      left: 1px;
      border-radius: 100%;
      transition: all 0.3s;
      width: 16px;
      height: 16px;
      background-color: #fff;
    }
  }
}

.hm-switch.is-checked {
  .hm-switch__core {
    border-color: #409eff;
    background-color: #409eff;
    .hm-switch__button {
      transform: translateX(20px);
    }
  }
}
</style>