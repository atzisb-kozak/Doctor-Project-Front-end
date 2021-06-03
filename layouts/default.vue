<template>
  <v-app>
    
   <v-app-bar
    height="60"
    dense
    dark
    app
    fixed
    >
      <v-app-bar-title>Navigation</v-app-bar-title>
        <NuxtLink class="link" to="/">Accueil</NuxtLink>
        <NuxtLink class="link" to="/login">Connexion</NuxtLink>
        <NuxtLink class="link" to="/login_doctor">Connexion Docteur</NuxtLink>
        <Nuxt-link class="link" to="/page_doctor">Espace Docteur</Nuxt-link>
        <v-spacer></v-spacer>
        <v-switch class="theme_switch"
        v-model="$vuetify.theme.dark"
        inset
        dense
        label="Night Mode"
        persistent-hint
      ></v-switch>
   </v-app-bar>

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
