<template>
  <span class="counter" :class="{'white': colorWhite}">
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
    },
    colorWhite: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
  .counter{
    color: $text-primary;
    font-weight: bold;
    font-size: 40px;
    transform: rotate(270deg);
    width: 45px;
    height: 45px;

    &__line{
      width: 6px;
      height: 32px;
      transform: rotate(270deg);
      float: right;
      position: absolute;
      top: 7px;
      left: 72px;
      background-color: $text-primary;
    }
  }

  .white .counter__line{
    background-color: $text-white;
  }

  .white .counter__number{
    color: $text-white;
  }
</style>
