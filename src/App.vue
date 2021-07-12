<template>
  <div id="app">
    <main-screen />
    <about-us />
    <our-achievements />
    <our-products />
    <our-documentation />
    <our-partners />
    <our-contacts />
    <footerSite ></footerSite>
  </div>

</template>

<script>
import mainScreen from "./components/mainScreen";
import aboutUs from "./components/aboutUs";
import ourAchievements from "./components/achievements";
import ourProducts from "./components/products";
import ourDocumentation from "./components/documentation";
import ourPartners from "./components/partners";
import ourContacts from "./components/contacts";
import footerSite from "./components/footer/footer";

export default {
  name: 'App',
  components: {
    mainScreen,
    aboutUs,
    ourAchievements,
    ourProducts,
    ourDocumentation,
    ourPartners,
    ourContacts,
    footerSite
  }
}
</script>

<style lang="scss">
//
</style>
