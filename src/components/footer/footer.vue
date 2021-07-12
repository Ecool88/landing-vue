<template>
  <footer class="footer">
    <div class="footer__go-up">
      <div class="go-up__title">Наверх</div>
      <div class="go-up__arrow"></div>
    </div>
    <div class="footer__container">
      <nav-footer />
      <description-footer />
    </div>
  </footer>
</template>

<script>
import navFooter from "./navFooter";
import descriptionFooter from "./descriptionFooter";
export default {
  name: "footer",
  components: {
    navFooter,
    descriptionFooter
  }
}
</script>

<style scoped lang="scss">
  .footer{
    width: 100%;
    height: 637px;
    background-image: url("../../assets/images/footer.png");
    padding: 125px 125px 125px 230px;
    position: relative;


    &__container{
      display: flex;
      justify-content: space-between;
    }

    &__go-up{
      position: absolute;
      bottom: 182px;
      left: 76px;
      transform: rotate(270deg);
    }


  }

  .go-up{
    &__title{
      color: $text-white;
      font-size: 13px;
    }

    &__arrow{
      position: absolute;
      bottom: -10px;
      left: 0;
      width: 90px;
      height: 2px;
      background-color: $text-white;


      &::before{
        content: '';
        position: absolute;
        top: 3px;
        left: 82px;
        background-color: $text-white;
        transform: rotate(135deg);
        width: 10px;
        height: 2px;
      }
      &::after{
        content: '';
        position: absolute;
        top: -3px;
        left: 82px;
        background-color: $text-white;
        transform: rotate(45deg);
        width: 10px;
        height: 2px;
      }
    }
  }
</style>
