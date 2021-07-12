<template>
  <div class="logo">
    <img class="logo__img" src="../../assets/images/explotation-documentation.png">
  </div>
</template>

<script>
export default {
  name: "logoDocumentation"
}
</script>

<style scoped lang="scss">
.logo{
  width: 50%;
  height: 100%;
  float: right;
  position: relative;


  &::before{
    content: '';
    border-top: 143px solid #FFFFFF;
    border-right: 143px solid transparent;
    position: absolute;
    top: 0;
    left: 0;
  }

  &__img{
   width: 100%;
   height: 100%;
  }
}
</style>
