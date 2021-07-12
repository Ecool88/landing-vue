<template>
  <nav class="nav-footer">
    <h5 class="nav-footer__title">
      Навигация
    </h5>
    <ul class="nav-footer__items">
      <li class="nav-footer__item">
        <a class="item__link" href="#">
          Главная
        </a>
      </li>
      <li class="nav-footer__item">
        <a class="item__link" href="#">
          Продукты
        </a>
      </li>
      <li class="nav-footer__item">
        <a class="item__link" href="#">
          Проекты
        </a>
      </li>
      <li class="nav-footer__item">
        <a class="item__link" href="#">
          Решения
        </a>
      </li>
      <li class="nav-footer__item">
        <a class="item__link" href="#">
          Вакансии
        </a>
      </li>
      <li class="nav-footer__item">
        <a class="item__link" href="#">
          Публикации
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "navFooter"
}
</script>

<style scoped lang="scss">
  .nav-footer{
    width: 200px;
    height: auto;

    &__title{
      font-size: 24px;
      font-weight: 500;
      color: $text-white;
      margin-bottom: 58px;
      position: relative;

      &::after{
        position: absolute;
        bottom: -30px;
        left: 0;
        content: '';
        background-color: $text-white;
        width: 110px;
        height: 2px;
      }
    }


    &__item{
      color: $text-white;
      font-size: 20px;
      position: relative;
      margin: 0 0 27px 27px;
      letter-spacing: 1px;

      &::before{
        content: '';
        position: absolute;
        top: 6px;
        left: -30px;
        background-color: $text-white;
        transform: rotate(45deg);
        width: 10px;
        height: 2px;
      }

      &::after{
        content: '';
        position: absolute;
        top: 12px;
        left: -30px;
        background-color: $text-white;
        transform: rotate(315deg);
        width: 10px;
        height: 2px;
      }
    }
  }
</style>
