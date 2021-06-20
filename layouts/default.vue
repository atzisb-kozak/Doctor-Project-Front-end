<template>
  <v-app>
    
   <v-app-bar
    height="60"
    dense
    dark
    app
    fixed
    >
      <v-app-bar-title><div style="font-size:1.5rem">Navigation</div></v-app-bar-title>
        <NuxtLink class="mr-10 ml-10" to="/">Accueil</NuxtLink>
        <v-divider vertical></v-divider>
        <NuxtLink class="mr-10 ml-10" to="/login">Connexion</NuxtLink>
        <v-spacer></v-spacer>
        <v-col
        cols="1">
          <v-switch class="mt-4 theme_switch"
          v-model="$vuetify.theme.dark"
          inset
          dense
          label="Night Mode"
          persistent-hint>
          </v-switch>
        </v-col>
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
