<template>
  <v-card class="overflow-hidden">
    <v-app-bar fixed color="white" elevate-on-scroll class="app_header">
      <v-btn
        icon
        depressed
        class="goback"
        v-if="$router.currentRoute.path == '/more'"
        @click="goBack"
        ><v-icon>mdi-chevron-left</v-icon></v-btn
      >
      <v-toolbar-title class="d-flex align-items-center"
        ><div class="logo_wrap">
          <img src="../res/pattern.png" alt="" />
        </div>
        <span class="site_name">Qazaq Oiy</span></v-toolbar-title
      >
    </v-app-bar>
  </v-card>
</template>

<script>
export default {
  name: "AppHeader",
  created() {},
  computed: {},
  methods: {
    goBack() {
      this.$router.push("/");
    },
  },
  mounted() {},
};
</script>

<style lang="scss" scoped>
</style>