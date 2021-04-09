<template>
  <v-app>

   <v-app-bar
      dense
      dark>
      <v-toolbar-title>Navigation</v-toolbar-title>
        <NuxtLink class="link" to="/">Accueil</NuxtLink>
        <NuxtLink class="link" to="/login">Login</NuxtLink>
    </v-app-bar>

    <v-main>
       <v-container fluid>

      <!-- If using vue-router -->
      <router-view></router-view>
       </v-container>
    </v-main>
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
