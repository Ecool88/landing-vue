<template>
  <section class="contacts">
    <contact-info />
    <div class="contacts__maps">
      <iframe src="https://yandex.ru/map-widget/v1/?ll=37.712165%2C55.786703&z=20" width="799px" height="753px" frameborder="1" allowfullscreen="true"></iframe>
    </div>
    <sidebar-contacts />
  </section>
</template>

<script>
import sidebarContacts from "./sidebarContacts";
import contactInfo from "./contactInfo";
export default {
  name: "contacts",
  components: {
    sidebarContacts,
    contactInfo
  }
}
</script>

<style scoped lang="scss">
  .contacts{
    height: 753px;
    width: 100%;
    display: flex;

    &__maps{
     width: 799px;
     height: 100%;

    }
  }
</style>
