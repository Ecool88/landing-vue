<template>
  <section>
    <sidebar-about-us />
    <content-about-us />
  </section>
</template>

<script>
import sidebarAboutUs from "./sidebarAboutUs";
import contentAboutUs from "./contentAboutUs";

export default {
  name: "aboutUs",
  components: {
    contentAboutUs,
    sidebarAboutUs
  }
}
</script>

<style scoped lang="scss">
  section{
    height: 512px;
    width: 100%;
  }
</style>
