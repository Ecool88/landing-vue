<template>
  <div class="sidebar">
    <h2 class="sidebar__title">
      CONTACT
    </h2>
    <div class="sidebar__wrapper-button">
      <el-button :title="'Вакансии'"/>
    </div>
  </div>
</template>

<script>
import elButton from '../elements/el-button'
export default {
  name: "sidebarContacts",
  components: {
    elButton
  }
}
</script>

<style scoped lang="scss">
  .sidebar{
    width: 327px;
    height: 100%;
    position: relative;

    &__title{
      font-size: 60px;
      font-weight: bold;
      transform: rotate(90deg);
      position: absolute;
      top: 352px;
      left: -30px;
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
