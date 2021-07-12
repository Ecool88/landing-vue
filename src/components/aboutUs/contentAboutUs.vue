<template>
  <div class="content-about">
    <el-headline :headline="'Почему выбирают нас?'"/>
    <div class="content-about__items">
      <block-about-us
        :title="'Квалицификация специалистов'"
        :description="'Постоянный рост квалификации наших специалистов обеспечивается непрерывным потоком инвестиций в обучающие курсы, сертификационные экзамены,\n'+
'а также в развитие собственной учебной базы.'"
      />
      <block-about-us
          :title="'Корпоративные принципы'"
          :description="'Все свои усилия мы направляем на достижение необходимого результата в кратчайший срок и в рамках запланированного бюджета. \n'+
'Мы ищем те самые 20% усилий, которые принесут 80% результата.'"
      />
      <block-about-us
          :title="'Ценовая политика ITFB Group'"
          :description="'Модель ценообразования является очень гибкой и зачастую формируется отдельно под каждого клиента в зависимости от требующихся результатов и уровня закрепленной ответственности.'"
      />
    </div>
  </div>
</template>

<script>
import elHeadline from '../elements/el-headline'
import blockAboutUs from "./blockAboutUs";

export default {
  name: "contentAboutUs",
  components: {
    elHeadline,
    blockAboutUs
  }
}
</script>

<style scoped lang="scss">
  .content-about{
    width: 1593px;
    height: 100%;
    display: flex;
    flex-direction: column;
    background-color: #F6F9FF;
    position: relative;
    padding: 100px 110px;


    &::before{
      content: '';
      border-top: 147px solid #FFFFFF;
      border-right: 147px solid transparent;
      position: absolute;
      top: 0;
      left: 0;
    }


    &__items{
      margin-top: 70px;
      display: flex;
      justify-content: space-evenly;
    }
  }
</style>
