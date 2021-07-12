<template>
  <div class="sidebar-products">
    <h2 class="sidebar-products__title">
      PRODUCTS
    </h2>
    <div class="sidebar-products__wrapper-button">
      <el-button :title="'Публикации'"/>
    </div>
  </div>
</template>

<script>
import elButton from "../elements/el-button"

export default {
  name: "sidebarProducts",
  components: {
    elButton
  }
}
</script>

<style scoped lang="scss">
  .sidebar-products{
    width: 317px;
    height: 100%;
    position: relative;
    float: right;
    background-color: #F6F9FF;

    &__title{
      font-size: 60px;
      font-weight: bold;
      transform: rotate(90deg);
      position: absolute;
      top: 367px;
      right: -19px;
      letter-spacing: 5px;
    }

    &__wrapper-button{
      height: 81px;
      width: 100%;
      position: absolute;
      bottom: 0;
      left: 0;
      letter-spacing: 2px;
    }
  }
</style>
