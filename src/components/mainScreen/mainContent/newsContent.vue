<template>
  <div class="news__container">
    <span class="news__date">{{date}}</span>
    <div class="news__subtitle">{{subtitle}}</div>
    <div class="news__content">{{content}}</div>
  </div>
</template>

<script>
export default {
  name: "newsContent",
  props: {
    date: {
      type: String,
      default: 'date'
    },
    subtitle: {
      type: String,
      default: 'subtitle'
    },
    content: {
      type: String,
      default: 'content'
    }
  }
}
</script>

<style lang="scss" scoped>
  .news{
    &__container{
      width: 450px;
      display: flex;
      flex-direction: column;
    }

    &__date{
      margin-top: 20px;
    }

    &__subtitle{
      margin-top: 20px;
      font-weight: bold;
    }

    &__content{
      margin: 20px 0 0 20px;
      width: 365px;
    }

  }
</style>
