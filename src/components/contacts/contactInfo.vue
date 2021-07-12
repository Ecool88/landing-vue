<template>
  <div class="contact-info">
    <el-headline class="contact-info__headline" :headline="'Контакты'" />
    <div class="contact-info__box">
      <div class="contact-info__office">
        <div class="contact-info__title">
          Основной офис:
        </div>
        <div class="contact-info__address">
          Малая Семеновская ул., д. 11А, стр. 4 кабинет 10 г. Москва, Россия, 107023
        </div>
      </div>
      <div class="contact-info__office">
        <div class="contact-info__title">
          Офис в Рязани:
        </div>
        <div class="contact-info__address">
          ул. Татарская, д. 21, офис 306
          г. Рязань, Россия, 390046
        </div>
      </div>
      <div class="contact-info__feedback">
        <div class="phone">
          <div class="contact-info__title">
            Телефон:
          </div>
          <div class="contact-info__address">
            +7 495 234-61-42
          </div>
        </div>
        <div class="mail">
          <div class="contact-info__title">
            Почта:
          </div>
          <div class="contact-info__address">
            mail@itfbgroup.ru
          </div>
        </div>
      </div>
        <div class="contact-info__wrapper-button">
          <el-button :title="'Связаться с нами'"/>
        </div>
      </div>
    </div>
</template>

<script>
import elHeadline from '../elements/el-headline';
import elButton from '../elements/el-button'
export default {
  name: "contactInfo",
  components: {
    elButton,
    elHeadline
  }
}
</script>

<style scoped lang="scss">
  .contact-info{
    width: 794px;
    height: 100%;
    padding: 100px 100px 70px;

    &__headline{
      margin-left: 75px;
    }

    &__box{
      padding: 65px 0 0 138px;
    }

    &__office:not(:first-child){
      margin-top: 50px;
    }

    &__title{
      font-size: 19px;
      color: #A19999;
    }

    &__address{
      margin-top: 15px;
      letter-spacing: 1px;
      font-size: 22px;
      color: #413F3F;
    }

    &__feedback{
      margin-top: 50px;
      display: flex;
      justify-content: space-between;
    }

    &__wrapper-button{
      margin-top: 50px;
      width: 395px;
      height: 81px;
      letter-spacing: 3px;
    }
  }
</style>
