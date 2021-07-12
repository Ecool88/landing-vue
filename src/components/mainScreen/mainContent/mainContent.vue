<template>
  <section class="main-block">
    <div class="main-block__content">
      <nav class="main-block__header navbar">

          <a href="#" class="navbar__brand">
            <img src="../../../assets/images/logo.svg" class="navbar__logo" alt="logo">
          </a>

          <ul class="navbar__items">
            <li class="navbar__item">
              <a href="#" class="navbar__link">Решения и услуги</a>
            </li>
            <li class="navbar__item">
              <a href="#" class="navbar__link">Проекты</a>
            </li>
            <li class="navbar__item">
              <a href="#" class="navbar__link">Контакты</a>
            </li>
          </ul>

      </nav>

      <div class="main-block__slogan slogan-block">
        <div class="slogan-block__container">
          <h2 class="slogan-block__title">IT-РЕШЕНИЯ ДЛЯ БИЗНЕСА</h2>
          <div class="slogan-block__subtitle">Повышаем эффективность бизнеса наших клиентов
            за счет внедрения качественных и современных решений</div>
        </div>
        <el-counter class="slogan-block__counter" :counter="'01'" :color-white="true"/>
      </div>
    </div>
    <div class="main-block__news item-news">
      <h5 class="item-news__title">Последние новости</h5>
      <div class="item-news__box">
        <news-content
          :date="'17/09'"
          :subtitle="'Мы создали EasyDoc'"
          :content="'ITFB EasyDoc это линейка продуктов, обеспечивающая быструю обработку различных клиентских документов по фотографии, из сканированного образа либо из видеопотока.'"
        />
        <news-content
          :date="'31/08'"
          :subtitle="'Oracle - для всех сфер бизнеса'"
          :content="'Компания ITFB Group, являясь партнером ORACLE Corporation уровня GOLD, поставила лицензии Oracle и сертификаты на техническую поддержку для предприятий промышленности нашей страны.'"
        />
      </div>
    </div>
  </section>
</template>

<script>
import elCounter from "../../elements/el-counter";
import newsContent from "./newsContent";

export default {
  name: "mainContent",
  components: {
    elCounter,
    newsContent
  }
}
</script>

<style lang="scss" scoped>

.main-block{
  width: 1287px;
  height: 100%;
  display: inline-block;
  position: relative;

  &__header{
    position: absolute;
    top: 40px;
    left: 95px;
    z-index: 1;
  }
}

.navbar{
  width: 675px;
  height: auto;
  display: flex;
  justify-content: space-between;

  &__items{
    display: flex;
    width: 435px;
    margin-top: 5px;
  }

  &__item:not(:first-child){
    margin-left: 55px;
  }

  &__link{
    font-size: 14px;
    color: $text-white;
    font-weight: 500;
    letter-spacing: .6px;
  }

  &__logo{
    width: 84px;
    height: 54px;
  }
}


.slogan-block{
  background: url("../../../assets/images/solutions-for-bussines.png") right center no-repeat;
  background-color: #000000;
  height: 646px;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;

  &::after{
    content: '';
    border-bottom: 145px solid #FFFFFF;
    border-left: 145px solid transparent;
    position: absolute;
    bottom: 0;
    right: 0;
  }

  &::before{
    content: '';
    display: block;
    position: absolute;
    top: 483px;
    right: 0;
    bottom: 0;
    left: 1123px;
    pointer-events: none;
    background: radial-gradient(circle, rgba(192, 182, 255, 0.6) 3px, transparent 10%);
    background-size: 21px 21px;
  }

  &__container{
    display: flex;
    flex-direction: column;
    width: 755px;
    margin-top: 40px;
  }

  &__title{
    color: $text-white;
    font-size: 37px;
    letter-spacing: 4px;
    font-weight: 800;
  }

  &__counter{
    position: absolute;
    bottom: 67px;
    left: 108px;
  }

  &__subtitle{
    width: 600px;
    color: $text-white;
    font-size: 20px;
    font-weight: 400;
    margin: 10px 0 0 10px;


    &::before{
      content: '';
      width: 3px;
      height: 42px;
      background-color: #C0B6FF;
      float: left;
    }
  }
}

.item-news{
  padding: 65px 150px 0 180px;


  &__title{
    font-size: 18px;
    font-weight: 500;
    letter-spacing: 2px;
  }

  &__box{
    display: flex;
  }
}
</style>
