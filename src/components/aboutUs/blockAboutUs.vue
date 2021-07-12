<template>
  <div class="item-block">
    <div class="item-block__title">
      {{title}}
    </div>
    <div class="item-block__desc">
      {{description}}
    </div>
  </div>
</template>

<script>
export default {
  name: "blockAboutUs",
  props: {
    title: {
      type: String,
      default: 'title'
    },
    description: {
      type: String,
      default: 'description'
    }
  }
}
</script>

<style scoped lang="scss">
  .item-block{
    width: 460px;
    height: 200px;
    margin-left: 32px;



    &__title{
      font-weight: 500;
      font-size: 22px;
      letter-spacing: 2.5px;
      white-space: nowrap;
    }


    &__desc{
      margin-top: 22px;
      font-size: 13px;
    }
  }
</style>
