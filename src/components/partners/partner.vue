<template>
  <a class="partner" href="#">
    <img :src="require('../../assets/images/' + src)" class="partner__logo">
    <div class="partner__desc" :style="{textAlign}">
      {{desc}}
    </div>
  </a>
</template>

<script>
export default {
  name: "partner",
  props: {
    src: {
      type: String,
      default: 'src'
    },
    desc: {
      type: String,
      default: 'desc'
    },
    textAlign: {
      type: String,
      default: 'right'
    }
  }
}
</script>

<style lang="scss" scoped>
  .partner{
    &__desc{
      font-size: 13px;
    }
  }
</style>
