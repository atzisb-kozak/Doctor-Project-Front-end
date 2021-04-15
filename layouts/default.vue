<template>
  <v-app>

   <v-toolbar
    height="70"
      dense
      dark>
      <v-toolbar-title>Navigation</v-toolbar-title>
        <NuxtLink class="link" to="/">Accueil</NuxtLink>
        <NuxtLink class="link" to="/login">Login</NuxtLink>
        <NuxtLink class="link" to="/login_doctor">Doc Login</NuxtLink>
        <v-spacer></v-spacer>
        <v-switch class="theme_switch"
        v-model="$vuetify.theme.dark"
        inset
        dense
        label="Night Mode"
        persistent-hint
      ></v-switch>
   </v-toolbar>

    <v-main>

      <!-- If using vue-router -->
      <router-view></router-view>

    </v-main>
     <v-footer padless>
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>Doctor.re</strong>
    </v-col>
  </v-footer>
  </v-app>
</template>

<script>
export default {
  data: () => ({ drawer: null }),
};
</script>

<style>
  .link
  {
    margin-left: 3rem;
    font-size: 1rem;
  }
</style>
