<template>
  <article class="news__container">
    <span class="news__date">{{date}}</span>
    <div class="news__subtitle">{{subtitle}}</div>
    <div class="news__content">{{content}}</div>
  </article>
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
      margin-left: 25px;
    }

    &__date{
      font-size: 14px;
      margin-top: 15px;
    }

    &__subtitle{
      font-weight: 500;
      font-size: 17px;
      margin-top: 10px;
      letter-spacing: 2px;
    }

    &__content{
      margin: 13px 0 0 33px;
      width: 365px;
      font-size: 14px;
    }

  }
</style>
