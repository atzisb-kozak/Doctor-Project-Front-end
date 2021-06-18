<template>
  <v-app>
    <v-main>
      <v-container fill-height fluid>
        <v-card 
          class="card rounded-xl mx-auto justify-center"
          dark
          width="500px"
          > 
          <v-row
            align="center"
            justify="center"
          >
            <v-card-title class="mt-2 mb-2">
              Connexion
            </v-card-title>
          </v-row>
          <v-form
            class="log_form"
            ref="form"
            v-model="valid"
            lazy-validation
          >
            <v-row
              align="center"
              class="ml-2 mr-2"
            >
              <v-text-field
                v-model="Username"
                :rules="usernameRules"
                class="rounded-pill"
                label="Pseudo"
                required
                outlined
              >
              </v-text-field>
            </v-row>
            <v-row
              align="center"
              class="ml-2 mr-2"
            >
              <v-text-field
              v-model="Password"
              :append-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="passwordRules"
              :type="show ? 'text' : 'password'"
              class="rounded-pill"
              label="Mot de passe"
              required
              outlined
              @click:append="show = !show"
              >
              </v-text-field>
            </v-row>
            <v-row
              align="center"
              justify="center"
            >
              <v-btn
              :disabled="!valid"
              color="success"
              class="mr-4 rounded-pill"
              @click="validate"
              >
                Validate
              </v-btn>
            </v-row>
          </v-form>
          <v-card-text>
            <v-row
              align="center"
              justify="center"
              class="mt-2"
            >
              <p>Pas encore inscrit ? <nuxt-link to="/register">Inscrivez-vous ici</nuxt-link></p>
              <p>Vous êtes l'un de nos medecins ? <nuxt-link to="doctors/doctor_login">
              C'est par ici</nuxt-link></p>
            </v-row>
          </v-card-text>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<style scoped>

.log_form{
    margin-left: 1rem;
    margin-right: 1rem;
}
.card{
  margin-left: 32.5%;
}
</style>

<script>
export default {
  data: () => ({
    show: false,
    Username: '',
    usernameRules: [
      v => !!v || 'Username is required',
    ],
    Password: '',
    passwordRules: [
      v => !!v || 'Password is required',
    ]
  }),
  methods: {
    validate () {
      this.$refs.form.validate();
    }
  },
  layout: 'nolayout'
};
</script>