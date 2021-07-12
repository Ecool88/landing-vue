<template>
  <div class="product">
    <div class="product__logo">
      <img class="product__img" :src="require('../../assets/images/' + src)"/>

      <div class="product__title">
        {{title}}
      </div>
    </div>
    <div class="product__description">
      <div class="product__text">
        {{description}}
      </div>
      <a href="#" class="product__more">
        Подробнее
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "blockProduct",
  props: {
    title: {
      type: String,
      default: 'title'
    },
    description: {
      type: String,
      default: 'description'
    },
    src: {
      type: String,
      default: 'src'
    }
  }
}
</script>

<style scoped lang="scss">
  .product{
    width: 390px;
    height: 400px;
    margin-left: 100px;
    position: relative;


    &__logo{
      height: 250px;
      width: 100%;
      position: relative;
      box-shadow: 2px 2px 10px 2px;

      &::before{
        content: '';
        width: 54px;
        height: 5px;
        background-color: #000;
        position: absolute;
        bottom: 0px;
        left: 0;
        z-index: 1;
      }

      &::after{
        content: 'PDF';
        background-color: #FFFFFF;
        color: $text-primary;
        width: 100px;
        height: 70px;
        position: absolute;
        bottom: 70px;
        left: 0;
        font-size: 35px;
        font-weight: bold;
        text-align: center;
        line-height: 80px;
      }
    }


    &__img{
      height: 100%;
      width: 100%;
    }

    &__title{
      position: absolute;
      bottom: 0;
      right: 0;
      width: 100%;
      height: 70px;
      background-color: #FFFFFF;
      color: $text-primary;
      font-weight: 600;
      font-size: 25px;
      text-align: right;
      line-height: 80px;
    }


    &__description{
      margin-top: 35px;
      font-size: 13px;
      line-height: 20px;
      text-align: left;
    }

    &__more{
      position: absolute;
      bottom: 0;
      right: 0;
      font-size: 17px;
      color: #767BF1;
    }

  }
</style>
