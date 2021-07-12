<template>
  <div id="app">
<!--    <img alt="Vue logo" src="./assets/logo.png">-->
<!--      <div class="wrapper-btn">-->
<!--        <vBtn :title="'Связаться с нами'"/>-->
<!--      </div>-->
<!--    <div class="example-image">-->

<!--    </div>-->
<!--    <div class="repeat-circle">-->

<!--    </div>-->
    <main-screen />
  </div>

</template>

<script>
// import vBtn from './components/elements/el-button'
import mainScreen from "./components/mainScreen/mainScreen";

export default {
  name: 'App',
  components: {
    // vBtn
    mainScreen
  }
}
</script>

<style lang="scss">
.wrapper-btn{
  width: 395px;
  height: 81px;
  font-weight: 700;
  font-size: 20px;
/*  оборачиваем кнопку и задае нужные нам размеры */
}
.example-image{
  height: 400px;
  width: 400px;
  background-color: aqua;
  position: relative;
}
.example-image::after{
  /*  так перекроем фото
  https://myrusakov.ru/css-skew-corner.html либо linear-gradient
  */
  content: '';
  border-bottom: 147px solid red;
  border-left: 147px solid transparent;
  position: absolute;
  bottom: 0;
  right: 0;
}

.example-image::before {
  content: '';
  display: block;
  position: absolute;
  top: 245px;
  right: 0;
  bottom: 0;
  left: 245px;
  //z-index: -1;
  pointer-events: none;
  background: radial-gradient(circle, black 5px, transparent 10%);
  background-size:20px 20px;
}

//.repeat-circle{
//  position: relative;
//  width: 220px;
//  height: 220px;
//  border: 2px solid black;
//}
//.repeat-circle::before {
//  display:block;
//  position: absolute;
//  top: 0;
//  left: 0;
//  width: 100px;
//  height: 100px;
//  content: '';
//  background-image: url('./assets/icons/Ellipse.png');
//  background-size: 5px 5px;
//  background-repeat: space;
//}
.repeat-circle {
  position: relative;
  height: 140px;
  width: 80px;
}

  .repeat-circle::after {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: -1;
  pointer-events: none;
    background: radial-gradient(circle, black 5px, transparent 10%),
    radial-gradient(circle, white 10%, white 10%);
    background-size:20px 20px;
}
</style>
