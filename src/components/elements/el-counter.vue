<template>
  <span class="counter">
    <span class="counter__number">{{counter}}</span>
    <span class="counter__line"></span>
  </span>
</template>

<script>
export default {
  name: "el-counter",
  props:{
    counter: {
      type: String,
      default: "01"
    }
  }
}
</script>

<style lang="scss" scoped>
  .counter{
    color: $text-white;
    font-weight: bold;
    font-size: 40px;
    transform: rotate(270deg);
    width: 45px;
    height: 45px;

    &__line{
      width: 6px;
      height: 32px;
      background-color: $text-white;
      transform: rotate(270deg);
      float: right;
      position: absolute;
      top: 7px;
      left: 72px;
    }
  }
</style>
