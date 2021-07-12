<template>
  <section class="documentation">
    <description-documentation />
    <logo-documentation />
  </section>
</template>

<script>
import descriptionDocumentation from "./descriptionDocumentation";
import logoDocumentation from "./logoDocumentation";
export default {
  name: "documentation",
  components: {
    descriptionDocumentation,
    logoDocumentation
  }
}
</script>

<style scoped lang="scss">
  .documentation{
    width: 100%;
    height: 571px;
  }
</style>
