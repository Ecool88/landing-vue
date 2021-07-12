<template>
  <div class="description">
    <h5 class="description__title">
      Решения и услуги
    </h5>
    <div class="description__rows">
      <div class="row__item">
        <div class="item__subtitle">
          <a href="#" class="subtitle__link">
            SOA/BPM
          </a>
        </div>
        <div class="item__desc">
          Заказная разработка
        </div>
        <div class="item__desc">
          Бюджетирование, бизнес-планирование
        </div>
      </div>
      <div class="row__item">
        <div class="item__subtitle">
          <a href="#" class="subtitle__link">
            BI
          </a>
        </div>
        <div class="item__desc">
          Тестирование
        </div>
        <div class="item__desc">
          Мультиканальная платформа
        </div>
      </div>
      <div class="row__item">
        <div class="item__subtitle">
          <a href="#" class="subtitle__link">
            ERP
          </a>
        </div>
        <div class="item__desc">
          Маскирование и виртуализация
        </div>
        <div class="item__desc">
          ITFB СЭД
        </div>
      </div>
      <div class="row__item">
        <div class="item__subtitle">
          <a href="#" class="subtitle__link">
            ECM
          </a>
        </div>
        <div class="item__desc">
          Программное обеспечение
        </div>
      </div>
      <div class="row__item">
        <div class="item__subtitle">
          <a href="#" class="subtitle__link">
            CRM
          </a>
        </div>
        <div class="item__desc">
          Оптическое распознавание документов
        </div>
        <div class="item__contacts">
          <div class="contact__mail">
            mail@itfbgroup.ru
          </div>
          <div class="contact__phone">
            +7 495 234-61-42
          </div>
          <div class="contact__copyright">
            © 2011—2019 ITFB Group
          </div>
        </div>
      </div>
      <div class="row__item">
          Консолидация финансовой отчетности по стандартам МСФО, <br>
          консолидация управленческой отчетности
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "descriptionFooter"
}
</script>

<style scoped lang="scss">
  .description{
    width: 1228px;
    height: auto;
    color: $text-white;
    font-weight: 500;


    &__title{
      letter-spacing: 1.5px;
      font-size: 24px;
      font-weight: 500;
      color: $text-white;
      margin-bottom: 55px;
      position: relative;

      &::after{
        position: absolute;
        bottom: -30px;
        left: 0;
        content: '';
        background-color: $text-white;
        width: 100%;
        height: 2px;
      }
    }

    &__rows{
      letter-spacing: 1px;
    }
  }

  .row__item{
    display: flex;
    margin-bottom: 28px;

    &:last-child{
      margin: -75px 0 0;
    }
  }
  .item{
    &__subtitle{
      width: 150px;
      height: auto;
      margin-right: 30px;
    }

    &__desc{
      letter-spacing: 1px;
      width: 485px;
      height: auto;
      font-size: 20px;
    }

    &__contacts{
      margin-left: auto;
      text-align: right;
    }
  }
  .contact{
    &__phone{
      margin: 12px 0;
    }
  }
</style>
