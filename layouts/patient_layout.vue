<template>
  <v-app>
    
   <v-app-bar
    height="60"
    dense
    dark
    app
    fixed
    >
    <v-menu
    rounded="1"
    offset-y
    min-width="200px">
    <template v-slot:activator="{ on }">
      <v-btn
      icon
      v-on="on">
        <v-avatar
        color="primary"
        size="46">
          <span class="white--text text-h5">{{user.initials}}</span>
        </v-avatar>
      </v-btn>
    </template>
    <v-card>
          <v-list-item-content class="justify-center">

            <div class="mx-auto text-center">

              <v-avatar
              color="primary"
              size="46">

                <span class="text-h5">{{ user.initials }}</span>

              </v-avatar>

              <h3>{{ user.fullName }}</h3>
              <p class="text-caption mt-1">
                {{ user.email }}
              </p>
              <v-divider class="my-3"></v-divider>
              <v-btn
                depressed
                rounded
                text
                @click="disconnect"
              >
                Disconnect
              </v-btn>
            </div>
          </v-list-item-content>
        </v-card>
    </v-menu>
        <NuxtLink class="link" to="/patient/patient_index">Accueil</NuxtLink>
        <NuxtLink class="link" to="/patient/patient_profile">Profil</NuxtLink>
        <NuxtLink class="link" to="/patient/patient_rdv">Rendez-vous</NuxtLink>
        <NuxtLink class="link" to="/bot">Assistant</NuxtLink>

        <v-spacer></v-spacer>
        <v-switch class="theme_switch"
        v-model="$vuetify.theme.dark"
        inset
        dense
        label="Night Mode"
        persistent-hint
      ></v-switch>
   </v-app-bar>

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
  data(){
    return {
      user:{
        initials: 'QS',
        fullName: 'Quentin SAM-LONG',
        email: 'test@test.com',
      },
    };
  },
  methods:{
    disconnect() {
      this.$router.push('/');
    }
  }
};
</script>

<style>
  .link
  {
    margin-left: 3rem;
    font-size: 1rem;
  }
</style>
