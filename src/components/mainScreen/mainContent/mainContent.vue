<template>
  <section class="content-block">
    <div class="body">
      <header>
        <nav class="navbar">
          <a href="#" class="navbar__brand">
            <img src="../../../assets/images/logo.svg" class="brand__logo" alt="logo">
          </a>

          <div class="navbar__container">
            <ul class="navbar__nav">
              <li class="nav__item">
                <a href="#" class="nav__link">Решения и услуги</a>
              </li>
              <li class="nav__item">
                <a href="#" class="nav__link">Проекты</a>
              </li>
              <li class="nav__item">
                <a href="#" class="nav__link">Контакты</a>
              </li>
            </ul>
          </div>

        </nav>
      </header>
      <div class="solutions-block">
        <div class="solutions-block__container">
          <h2 class="solutions-block__title">IT-решения для бизнеса</h2>
          <div class="solutions-block__subtitle">Повышаем эффективность бизнеса наших клиентов
            за счет внедрения качественных и современных решений</div>
        </div>
        <el-counter class="counter" :counter="'01'"/>
      </div>
    </div>
    <div class="news">
      <div class="news__title">Последние новости</div>
      <div class="news__box">
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

header{
  position: absolute;
  top: 50px;
  left: 100px;
  z-index: 1;
}

.navbar{
  width: 650px;
  height: auto;
  display: flex;
  justify-content: space-between;

  &__nav{
    display: flex;
    justify-content: space-between;
  }
}

.nav{
  &__item{
    margin-right: 50px;
  }

  &__link{
    font-size: 13px;
    color: $text-white;
    font-weight: 600;
  }
}


.content-block{
  width: 67%;
  height: 100%;
  display: inline-block;
  position: relative;
}



.solutions-block{
  background: url("../../../assets/images/solutions-for-bussines.png") right center no-repeat;
  background-color: #000000;
  width: 100%;
  height: 646px;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;

  &::after{
    content: '';
    border-bottom: 147px solid #FFFFFF;
    border-left: 147px solid transparent;
    position: absolute;
    bottom: 0;
    right: 0;
  }

  &::before{
    content: '';
    display: block;
    position: absolute;
    top: 487px;
    right: 0;
    bottom: 0;
    left: 1127px;
    pointer-events: none;
    background: radial-gradient(circle, rgba(192, 182, 255, .6) 5px, transparent 10%);
    background-size:20px 20px;
  }

  &__container{
    display: flex;
    flex-direction: column;
    width: 600px;
    height: auto;
  }

  &__title{
    color: $text-white;
    font-size: 40px;
    font-weight: bold;
  }

  &__subtitle{
    color: $text-white;
    font-size: 20px;
    font-weight: 600;

    &::before{
      content: '';
      width: 3px;
      height: 42px;
      background-color: #C0B6FF;
      float: left;
    }
  }
}

.counter{
  position: absolute;
  bottom: 65px;
  left: 110px;
}

.news{
  height: 324px;
  padding: 60px 150px 0 150px;

  &__box{
    display: flex;
  }

  &__title{
    font-size: 19px;
    font-weight: bold;
  }
}

</style>
