<template>
  <section>
    <div class="header__contact">
      <ul class="contact">
        <li class="contact__item">
          <a href="#" class="contact__link">
            <img src="../../../assets/icons/mail.png" alt="#" class="contact__icon">
            <span class="contact__text">mail@itfbgroup.ru</span>
          </a>
        </li>
        <li class="contact__item">
          <a href="#" class="contact__link">
            <img src="../../../assets/icons/phone.png" alt="#" class="contact__icon">
            <span class="contact__text">+7 495 234-61-42</span>
          </a>
        </li>
        <li class="contact__item">
          <a href="#" class="contact__link">
            <img src="../../../assets/icons/location.png" alt="#" class="contact__icon">
            <span class="contact__text">Москва, ул. Малая Семеновская д.11 к.4</span>
          </a>
        </li>
      </ul>
      <span class="hamburger__menu">
        <span class="hamburger__item"></span>
        <span class="hamburger__item"></span>
        <span class="hamburger__item"></span>
      </span>
    </div>

    <form action="" class="form">
      <h5 class="form__title">Связь с нами</h5>

      <div class="form__item">
        <label class="form__label" >Имя</label>
        <input type="text" class="form__input">
      </div>

      <div class="form__item">
        <label class="form__label" >E-mail</label>
        <input type="text" class="form__input">
      </div>

      <div class="form__item">
        <label class="form__label" >Телефон</label>
        <input type="text" class="form__input">
      </div>


      <div class="form__item">
        <label class="form__label" >Комментарий</label>
        <input type="text" class="form__input">
      </div>

      <span class="comment-length">0 / 120</span>

      <el-button :title="'Отправить'"/>

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
  section {
    width: 33%;
    display: inline-block;
    padding: 10px 55px;
  }

  .header__contact{
    display: flex;
  }

  .contact {
    width: 420px;
    height: auto;
    display: flex;
    justify-content: flex-end;
    flex-wrap: wrap;

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
      font-weight: 500;
    }
  }

  .hamburger{
    &__menu{
      width: 25px;
      height: 16px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin-top: 20px;
    }
    &__item{
      background-color: $text-primary;
      width: 100%;
      height: 2px;
    }
  }

  .form{
    width: 395px;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: flex-end;

    &__title{
      font-size: 26px;
      font-weight: bold;
      margin: 0;
    }

    &__item{
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      width: 100%;
      height: 30px;
      position: relative;
      margin-top: 50px;
    }

    &__label{
      position: absolute;
      bottom: 20px;
      font-size: 16px;
      color: $text-primary;
    }

    &__input{
      width: 100%;
      border: none;
      border-bottom: 1px solid $text-primary;
    }
  }

  .comment-length{
    margin-bottom: 10px;
  }


</style>
