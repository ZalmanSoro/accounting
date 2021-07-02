<template>
  <v-app>
    <app-bar @login="login"></app-bar>
    <login :dialog="dialog" />
    <v-main> </v-main>
  </v-app>
</template>

<script>
import AppBar from "./components/AppBar.vue";
import Login from "./components/Login.vue";

export default {
  name: "App",
  components: {
    AppBar,
    Login,
  },
  data: () => ({
    dialog: false,
  }),
  methods: {
    login() {
      this.dialog = true;
    },
  },
};
</script>

<style>

</style>