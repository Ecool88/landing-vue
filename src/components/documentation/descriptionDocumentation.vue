<template>
  <div class="description">
    <el-counter class="description__counter" :counter="'05'"/>
    <el-headline class="description__title" :headline="'Эксплуатационная документация'"/>
    <div class="description__text">
      Составление методической и эксплуатационной документации, обучение пользователей, введение системы в эксплуатацию
      <div class="description__wrapper-button">
        <el-button :title="'Подробнее'"/>
      </div>
      <div class="description__carousel slider">
        <span class="slider__arrow-left"></span>
        <span class="slider__counter">04 / 05</span>
        <span class="slider__arrow-right"></span>
      </div>
    </div>
  </div>
</template>

<script>
import elCounter from "../elements/el-counter"
import elHeadline from "../elements/el-headline"
import elButton from "../elements/el-button"
export default {
  name: "descriptionDocumentation",
  components: {
    elCounter,
    elHeadline,
    elButton
  }
}
</script>

<style scoped lang="scss">
  .description{
    width: 50%;
    height: 100%;
    float: left;
    position: relative;
    padding: 80px 175px;

    &::before{
      content: '';
      display: block;
      position: absolute;
      height: 143px;
      width: 81px;
      bottom: 0;
      left: 4px;
      pointer-events: none;
      background: radial-gradient(circle, rgba(192, 182, 255, 0.6) 3px, transparent 10%);
      background-size: 20px 21px;
    }

    &::after{
      content: '04';
      position: absolute;
      top: -38px;
      left: 632px;
      font-size: 160px;
      font-weight: bold;
      color: rgba(192, 182, 255, 0.3);
    }

    &__counter{
      position: absolute;
      bottom: 136px;
      left: 111px;
    }

    &__title{
      white-space: nowrap;
      letter-spacing: 2px;
    }


    &__text{
      margin: 60px 0 0 58px;
      letter-spacing: 1px;
      width: 600px;
    }

    &__wrapper-button{
      letter-spacing: 3px;
      width: 212px;
      height: 53px;
      margin-top: 50px;
    }
  }
  .slider{
    text-align: center;
    margin: 75px auto 0;
    width: 300px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    &__counter{
      font-size: 18px;
    }

    &__arrow-left{
      width: 50px;
      height: 1px;
      background-color: $text-primary;
      position: relative;
      &::after{
        content: '';
        width: 6px;
        height: 1px;
        position: absolute;
        background-color: $text-primary;
        transform: rotate(45deg);
        top: 2px;
        left: 0px;
      }
      &::before{
        content: '';
        width: 6px;
        height: 1px;
        position: absolute;
        background-color: $text-primary;
        transform: rotate(135deg);
        top: -2px;
        left: 0px;
      }
    }

    &__arrow-right{
      width: 50px;
      height: 1px;
      background-color: $text-primary;
      position: relative;
      &::after{
        content: '';
        width: 6px;
        height: 1px;
        position: absolute;
        background-color: $text-primary;
        transform: rotate(135deg);
        top: 2px;
        right: 0px;
      }
      &::before{
        content: '';
        width: 6px;
        height: 1px;
        position: absolute;
        background-color: $text-primary;
        transform: rotate(45deg);
        top: -2px;
        right: 0px;
      }
    }
  }
</style>
