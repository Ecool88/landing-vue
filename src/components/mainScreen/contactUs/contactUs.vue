<template>
  <section class="contact">
    <div class="contact-header">
      <ul class="contact-header__items">
        <li class="contact-header__item">
          <a href="#" class="contact-header__link">
            <img src="../../../assets/icons/mail.png" alt="#" class="contact-header__icon">
            <span class="contact-header__text">mail@itfbgroup.ru</span>
          </a>
        </li>
        <li class="contact-header__item">
          <a href="#" class="contact-header__link">
            <img src="../../../assets/icons/phone.png" alt="#" class="contact-header__icon">
            <span class="contact-header__text">+7 495 234-61-42</span>
          </a>
        </li>
        <li class="contact-header__item">
          <a href="#" class="contact-header__link">
            <img src="../../../assets/icons/location.png" alt="#" class="contact-header__icon">
            <span class="contact-header__text">Москва, ул. Малая Семеновская д.11 к.4</span>
          </a>
        </li>
      </ul>
      <span class="contact-header__menu hamburger-menu">
        <span class="hamburger-menu__item"></span>
        <span class="hamburger-menu__item"></span>
        <span class="hamburger-menu__item"></span>
      </span>
    </div>

    <form action="" class="contact-form">
      <legend class="contact-form__title">Связь с нами</legend>

      <ul class="contact-form__items">
        <li class="contact-form__item">
          <label class="contact-form__label" >Имя</label>
          <input type="text" class="contact-form__input">
        </li>

        <li class="contact-form__item">
          <label class="contact-form__label" >E-mail</label>
          <input type="text" class="contact-form__input">
        </li>

        <li class="contact-form__item">
          <label class="contact-form__label" >Телефон</label>
          <input type="text" class="contact-form__input">
        </li>


        <li class="contact-form__item">
          <label class="contact-form__label" >Комментарий</label>
          <input type="text" class="contact-form__input">

        </li>
      </ul>


      <el-button class="contact-form__btn" :title="'Отправить'"/>

    </form>
  </section>
</template>

<script>
import elButton from '../../elements/el-button'
export default {
  name: "contactUs",
  components: {
    elButton
  }
}
</script>

<style lang="scss" scoped>
  .contact {
    width: 633px;
    display: inline-block;
    padding: 50px 80px;


    &-header{
      display: flex;

      &__items{
        width: 420px;
        height: 90px;
        display: flex;
        justify-content: flex-end;
        flex-wrap: wrap;
      }

      &__link {
        color: $text-primary;
        line-height: 25px;

        &:first-child{
          margin-right: 40px;
        }
      }

      &__icon {
        width: 14px;
        height: 14px;
        margin-right: 16px;


      }

      &__text{
        font-size: 15px;
        font-weight: 400;
      }
    }

    &-form{
      height: auto;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      margin-top: 90px;

      &__title{
        font-size: 25px;
        font-weight: bold;
        letter-spacing: 2px;
      }

      &__items{
        width: 395px;
      }

      &__item{
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        width: 100%;
        height: 30px;
        position: relative;
        margin-top: 50px;

        &:last-child::after{
          content: '0 / 120';
          font-size: 12px;
          color: $text-primary;
        }
      }

      &__label{
        position: absolute;
        bottom: 20px;
        font-size: 17px;
      }

      &__input{
        width: 100%;
        border: none;
        border-bottom: 1px solid $text-primary;
      }

      &__btn{
        margin-top: 70px;
        width: 395px;
        height: 65px;
        font-weight: 600;
        letter-spacing: 1px;
      }
    }
  }


  .hamburger-menu{
      width: 25px;
      height: 16px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-top: 9px;
      margin-left: 27px;

    &__item{
      background-color: $text-primary;
      width: 100%;
      height: 2px;
    }
  }
</style>
