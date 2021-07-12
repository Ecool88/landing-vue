<template>
  <h3 class="headline" :class="{'white': colorWhite}">
    {{headline}}
  </h3>
</template>

<script>
export default {
  name: "el-headline",
  props: {
    headline: {
      type: String,
      default: 'headline'
    },
    colorWhite: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped lang="scss">
  .headline{
    font-size: 35px;
    height: 35px;
    font-weight: bold;
    display: inline-block;
    position: relative;
    color: $text-primary;
    letter-spacing: 2px;

    &::after{
      content: '';
      width: 54px;
      height: 4px;
      background-color: $text-primary;
      position: absolute;
      bottom: -30px;
      left: 0;
    }
  }


  .white::after{
    background-color: $text-white;
  }

  .white{
    color: $text-white;
  }
</style>
