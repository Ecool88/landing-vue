<template>
  <aside class="sidebar-about">
    <el-counter class="sidebar-about__counter" :counter="'02'"/>
    <h2 class="sidebar-about__title">
      ABOUT US
    </h2>
    <div class="sidebar-about__wrapper-button">
      <el-button :title="'Наши клиенты'"/>
    </div>
  </aside>
</template>

<script>
import elButton from '../elements/el-button'
import elCounter from '../elements/el-counter'

export default {
  name: "sidebarAboutUs",
  components: {
    elButton,
    elCounter
  }
}
</script>

<style scoped lang="scss">
  .sidebar-about{
    width: 327px;
    height: 100%;
    float: left;
    position: relative;


    &__title{
      font-size: 60px;
      font-weight: bold;
      transform: rotate(270deg);
      position: absolute;
      top: 176px;
      right: -85px;
      letter-spacing: 6px;
    }

    &__counter{
      position: absolute;
      bottom: 112px;
      left: 107px;
      color: $text-primary;
    }


    &__wrapper-button{
      height: 80px;
      width: 100%;
      letter-spacing: 3px;
      position: absolute;
      bottom: 0;
      left: 0;
    }


    &::before{
      content: '';
      display: block;
      position: absolute;
      height: 146px;
      width: 80px;
      top: -5px;
      right: 5px;
      bottom: 0;
      left: 3px;
      pointer-events: none;
      background: radial-gradient(circle, rgba(192, 182, 255, 0.6) 3px, transparent 10%);
      background-size: 21px 21px;
    }
  }
</style>
