<template>
  <button class="el-button">
      <span>{{title}}</span>
  </button>
</template>

<script>
export default {
  name: "el-button",
  data() {
    return {}
  },
  props: {
    title: {
      type: String,
      default: 'button'
    }
  }
}
</script>

<style lang="scss">
  .el-button{
    background-color: $bg-color-blue;
    border-color: $bg-color-blue;
    color: $text-white;
    display: flex;
    height: 100%;
    width: 100%;
    font-weight: inherit;
    font-size: inherit;
  }
  span{
    margin: auto;
    padding: 15px 35px;
    font-weight: inherit;
    font-size: inherit;
  }
</style>
