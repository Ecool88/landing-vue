<template>
  <div class="content-products">
    <el-headline class="content-products__headline" :headline="'Продукты ITFB Group'"/>
    <el-counter class="content-products__counter" :counter="'04'"/>
    <div class="content-products__container">
      <block-product
        :title="'PHOTOPAY'"
        :description="'Используйте новую технологию распознавания квитанций - фотоплатеж. Сфотографируйте \n'+
'квитанцию в мобильном банке, автоматически заполним все необходимые платежные реквизиты.'"
        :src="'photopay.png'"
      />
      <block-product
          :title="'IDREADER'"
          :description="'Веб-приложение для управления задачами\n'+
'распознавания, просмотра результатов распознавания,\n'+
'управления справочниками и настройками системы.'"
          :src="'idreader.png'"
      />
      <block-product
          :title="'CLASSIFFICATOR'"
          :description="'Классификация и сортировка\n'+
'документов в режиме реального\n'+
'времени при потоковом сканировании. Отложенная(«по требованию»), классификация и сортировка\n'+
'«исторических» архивов.'"
          :src="'classificator.png'"
      />
    </div>
  </div>
</template>

<script>
import elHeadline from "../elements/el-headline"
import blockProduct from "./blockProduct";
import elCounter from "../elements/el-counter"
export default {
  name: "contentProducts",
  components: {
    elHeadline,
    blockProduct,
    elCounter
  }
}
</script>

<style scoped lang="scss">
  .content-products{
    width: 1593px;
    height: 100%;
    float: left;
    position: relative;

    &::before{
      content: '';
      display: block;
      position: absolute;
      height: 152px;
      width: 80px;
      bottom: 0px;
      left: 4px;
      pointer-events: none;
      background: radial-gradient(circle, rgba(192, 182, 255, 0.6) 3px, transparent 10%);
      background-size: 21px 21px;
    }

    &__container{
      display: flex;
      padding: 225px 0;
      margin-left: 115px;
    }


    &__counter{
      position: absolute;
      bottom: 145px;
      left: 120px;
    }

    &__headline{
      position: absolute;
      left: 184px;
      top: 108px;
    }
  }
</style>
