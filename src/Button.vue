<template>
  <button :class="[type]">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: 'default'
    }
  },
  data() {
    return {}
  }
};
</script>

<style lang="less">
button{
  border: 1px solid #eee;
  border-radius: 4px;
  padding: 12px 20px;
  cursor: pointer;
  background: #fff;
  font-size: 14px;
  line-height: 1;
  white-space: nowrap;
  transition: all .1s;
  &:focus{
    outline: none;
  }
  &.default{
    border-color:#dcdfe6;
    color: #606266;
    &:hover{
      color: #409eff;
      border-color: #c6e2ff;
      background-color: #ecf5ff;
    }
  }
  &.primary{
    color: #fff;
    background-color: #409eff;
    border-color: #409eff;
    &:hover{
      background: #66b1ff;
      border-color: #66b1ff;
      color: #fff;
    }
  }
}
</style>