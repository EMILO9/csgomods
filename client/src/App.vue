<template>
  <v-app>
      <v-app-bar app color="#ffffff">
        <v-toolbar-title class="title" @click="goTo({ path: `/` })">CSGOMods</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn @click="goTo({ path: `/login` })" class="button" color="primary" depressed>Login</v-btn>
        <v-btn @click="goTo({ path: `/signup` })" class="button" depressed>Signup</v-btn>
        <v-btn @click="goTo({ path: `/account` })" class="button" color="primary" depressed><v-icon left>mdi-account</v-icon>My account</v-btn>
        <v-btn class="button" color="error" depressed>Logout</v-btn>
        <v-btn @click="goTo({ path: `/upload` })" class="button" color="primary" depressed>Upload mod<v-icon right>mdi-cloud-upload</v-icon></v-btn>
        <v-btn @click="goTo({ path: `/cart` })" class="button" color="primary" depressed><v-icon left>mdi-cart</v-icon>00.00 (0)</v-btn>
      </v-app-bar>
    <v-main>
      <router-view></router-view>
    </v-main>
      <v-footer color="#ffffff">
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>CSGOMods</strong>
    </v-col>
  </v-footer>
  </v-app>
</template>

<script>

export default {
  name: "App",
  data: () => ({
    //
  }),
  methods: {
    goTo(route) {
      this.$router.push(route).catch(err => err)
    }
  }
};
</script>
