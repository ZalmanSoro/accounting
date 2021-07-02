<template>
  <div>
    <v-app-bar dense app color="primary" dark>
      <v-app-bar-title>חשבונאות סאסי בע"מ</v-app-bar-title>
      <v-spacer />
      <v-btn dark small dense outlined @click="login">LOGIN</v-btn>
      <div class="mr-2">
        <v-avatar color="white"
          ><v-icon class="primary">mdi-account</v-icon></v-avatar
        >
      </div>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  methods: {
    login() {
      this.$emit("login");
    },
  },
};
</script>

<style>
</style>