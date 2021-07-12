<template>
  <section class="products">
    <content-products />
    <sidebar-products />
  </section>
</template>

<script>
import contentProducts from "./contentProducts";
import sidebarProducts from "./sidebarProducts";
export default {
  name: "products",
  components: {
    sidebarProducts,
    contentProducts
  }
}
</script>

<style scoped lang="scss">
.products{
  height: 800px;
  width: 100%;
}
</style>
