<template>
  <main>
    <main-content />
    <contact-us />
  </main>
</template>

<script>
import contactUs from "./contactUs/contactUs";
import mainContent from "./mainContent/mainContent";
export default {
  name: "mainScreen",
  components: {
    contactUs,
    mainContent
  }
}
</script>

<style scoped>
  main{
    width: 100%;
    height: 970px;
    display: flex;
  }
</style>
