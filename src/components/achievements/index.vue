<template>
  <section class="achievements-block">
    <el-headline class="achievements-block__headline" :headline="'Достижения'" :color-white="true"/>
    <el-counter class="achievements-block__counter" :color-white="true" :counter="'03'"/>
    <widget-achievment
      class="achievements-block__outer-radius"
      :count="'10'"
      :description="'Более 10-ти лет опыта в создании <br> крупных IT-проектов'"
    />
    <widget-achievment
        class="achievements-block__middle-radius"
        :count="'15'"
        :description="'Более 15 передовых услуг и решений для повышения эффективности вашего бизнеса'"
    />
    <widget-achievment
        class="achievements-block__inner-radius"
        :count="'100'"
        :description="'Более 100 успешных <br> проектов'"
    />
  </section>
</template>

<script>
import widgetAchievment from "./widgetAchievment";
import elHeadline from "../elements/el-headline"
import elCounter from "../elements/el-counter"

export default {
  name: "achievements-block",
  components: {
    widgetAchievment,
    elHeadline,
    elCounter
  }
}
</script>

<style scoped lang="scss">
  .achievements-block{
    width: 100%;
    height: 590px;
    background-image: url("../../assets/images/achievments.png");
    position: relative;
    overflow: hidden;

    &::before{
      content: '';
      display: block;
      position: absolute;
      height: 145px;
      width: 80px;
      bottom: 0;
      left: 0;
      pointer-events: none;
      background: radial-gradient(circle, rgba(192, 182, 255, 0.6) 3px, transparent 10%);
      background-size: 21px 21px;
    }

    &__outer-radius{
      position: absolute;
      top: 190px;
      left: 368px;


      &::before{
        border: solid 3px #939BE0;
        border-radius: 50%;
        box-sizing: border-box;
        content: '';
        position: absolute;
        top: -481px;
        left: 40px;
        width: 1600px;
        height: 1600px;
      }
    }


    &__middle-radius{
      position: absolute;
      top: 80px;
      left: 847px;


      &::before{
        border: solid 3px #939BE0;
        border-radius: 50%;
        box-sizing: border-box;
        content: '';
        position: absolute;
        top: -101px;
        left: -107px;
        width: 1250px;
        height: 1250px;
      }
    }


    &__inner-radius{
      position: absolute;
      top: 387px;
      left: 1037px;


      &::before{
        border: solid 3px #939BE0;
        border-radius: 50%;
        box-sizing: border-box;
        content: '';
        position: absolute;
        top: -138px;
        left: 19px;
        width: 900px;
        height: 900px;
      }
    }

    &__headline{
      position: absolute;
      top: 100px;
      left: 175px;
    }

    &__counter{
      position: absolute;
      bottom: 112px;
      left: 108px;
    }
  }
</style>
