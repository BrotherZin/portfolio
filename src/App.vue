<template>
  <v-app>
    <app-header></app-header>

    <router-view />
    <app-footer></app-footer>
  </v-app>
</template>

<script>
import AppHeader from "@/components/AppHeader";
import AppFooter from "@/components/AppFooter";
export default {
  name: "App",
  components: {
    AppHeader,
    AppFooter,
  },

  data: () => ({
    //
  }),
};
</script>
<style lang="less">
.typer {
  color: white;
  z-index: 100;
  position: relative;
  * {
    color: white !important;
  }
}
</style>
