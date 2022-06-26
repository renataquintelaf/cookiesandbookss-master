<script>
import HeaderComp from "@/components/template/HeaderComp.vue";
import MenuLateral from "@/components/template/MenuLateral.vue";
import FooterComp from "@/components/template/FooterComp.vue";

export default {
  components: { HeaderComp, MenuLateral, FooterComp },
};
</script>

<template>
  <HeaderComp />
  <MenuLateral />
  <main><RouterView /></main>
  <FooterComp />
</template>
<style>
#app {
  max-height: 1200px;
  margin: 0 auto;
  height: 100vh;
  font-weight: normal;
}

main {
  height: 700px;
}
</style>
