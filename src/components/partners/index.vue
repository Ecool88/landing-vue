<template>
  <section class="partners">
    <el-headline :headline="'Партнеры'"/>
    <div class="partners__container">
      <div class="partners__first-line">
        <partner
            :src="'sail-point.png'"
            :desc="'Sailpoint'"
            :text-align="'left'"
        />
        <partner
            :src="'abbyy.png'"
            :desc="'ABBYY Corporate Projects Gold Partner'"
            :text-align="'center'"
        />
        <partner
            :src="'ibm.png'"
            :desc="'IBM Authorized Partner'"
            :text-align="'center'"
        />
        <partner
            :src="'qlik.png'"
            :desc="'Qlik Tech'"
        />
        <partner
            :src="'oracle.png'"
            :desc="'Oracle Gold Partner'"
        />
      </div>
      <div class="partners__second-line">
        <partner
            :src="'tibco.png'"
            :desc="'Tibco'"
            :text-align="'left'"
        />
        <partner
            :src="'delphix.png'"
            :desc="'Delphix'"
            :text-align="'center'"
        />
        <partner
            :src="'rsa.png'"
            :desc="'RSA Security'"
        />
      </div>
      <div class="partners__third-line">
        <partner
            :src="'iso.png'"
            :desc="'SO 27001:2013'"
            :text-align="'center'"
        />
      </div>
    </div>
    <el-counter class="partners__counter" :counter="'06'"/>
  </section>
</template>

<script>
import partner from "./partner";
import elHeadline from '../elements/el-headline';
import elCounter from '../elements/el-counter'
export default {
  name: "partners",
  components: {
    partner,
    elHeadline,
    elCounter
  }
}
</script>

<style scoped lang="scss">
  .partners{
    height: 837px;
    width: 100%;
    position: relative;
    padding: 100px 175px;

    &::before{
      content: '';
      display: block;
      position: absolute;
      height: 143px;
      width: 81px;
      bottom: 2px;
      left: 2px;
      pointer-events: none;
      background: radial-gradient(circle, rgba(192, 182, 255, 0.6) 3px, transparent 10%);
      background-size: 20px 21px;
    }

    &__container{
      display: flex;
      flex-direction: column;
      height: 525px;
      justify-content: space-between;
      margin-top: 80px;
    }

    &__counter{
      position: absolute;
      bottom: 125px;
      left: 107px;
    }


    &__first-line{
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    &__second-line{
      display: flex;
      justify-content: space-evenly;
      align-items: center;
    }

    &__third-line{
      display: flex;
      justify-content: space-evenly;
      align-items: center;
    }
  }
</style>
