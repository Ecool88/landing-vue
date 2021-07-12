<template>
  <div class="widget">
    <div class="widget__outer-radius">
      <div class="widget__middle-radius">
        <div class="widget__inner-radius">
          <span class="widget__count">
            {{count}}
          </span>
        </div>
      </div>
    </div>
    <div class="widget__description" v-html="description">
    </div>
  </div>
</template>

<script>
export default {
  name: "widgetAchievment",
  props: {
    count: {
      type: String,
      default: 'count'
    },
    description: {
      type: String,
      default: 'description'
    }
  }
}
</script>

<style scoped lang="scss">
  .widget{
    display: inline-block;
    width: 670px;
    height: 140px;
    display: flex;
    justify-content: space-evenly;
    align-items: center;


    &__outer-radius{
      width: 140px;
      height: 140px;
      border-radius: 50%;
      background-color: #D2CDCD;
      position: relative;
    }

    &__middle-radius{
      width: 98px;
      height: 98px;
      border-radius: 50%;
      background-color: #EAE7E7;
      position: absolute;
      top: 0;
      left: 0;
      margin: auto;
      right: 0;
      bottom: 0;
    }

    &__inner-radius{
      width: 55px;
      height: 55px;
      border-radius: 50%;
      background-color: rgba(3, 27, 255, .3);
      position: absolute;
      top: 0;
      left: 0;
      margin: auto;
      right: 0;
      bottom: 0;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    &__count{
      width: auto;
      height: auto;
      color: $text-white;
      font-size: 40px;
      font-weight: bold;
    }

    &__description{
      color: $text-white;
      font-size: 20px;
      font-weight: bold;
      width: 490px;
      z-index: 1;
    }





  }
</style>
