<template>
  <div class="ground">
    <HeaderVue></HeaderVue>
    <MainVue/>
    <FooterVue></FooterVue>
  </div>
</template>

<script>
import FooterVue from "./Footer.vue";
import HeaderVue from "./Header.vue";
import MainVue from "./Main.vue";
export default {
  name: "GroundVue",
  components: {
    HeaderVue,
    FooterVue,
    MainVue,
  },
};
</script>

<style scoped>
</style>
