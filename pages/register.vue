<template>
  <v-app>
    <v-main>
      <v-container fill-height fluid>
        <v-card 
          class="card rounded-xl mx-auto justify-center"
          dark
          width="500px"
        >
          <v-row align="center" justify="center">
            <v-card-title class="mt-2 mb-2">
              Inscription
            </v-card-title>
          </v-row>
          <v-form class="reg_form"
          ref="form"
          v-model="valid"
          lazy-validation
          >
          <v-row
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              v-model="Firstname"
              :rules="firstnameRules"
              label="Prénom"
              class="rounded-pill"
              required
              outlined
            ></v-text-field>
          </v-row>
          <v-row
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              v-model="Lastname"
              :rules="lastnameRules"
              label="Nom"
              class="rounded-pill"
              required
              outlined
            ></v-text-field>
          </v-row>
          <v-row
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              v-model="Username"
              :rules="usernameRules"
              label="Pseudo"
              class="rounded-pill"
              required
              outlined
            ></v-text-field>
          </v-row>

          <v-row 
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              v-model="Age"
              :rules="ageRules"
              label="Age"
              type="number"
              class="rounded-pill"
              required
              outlined
            ></v-text-field>
          </v-row>

           <v-row 
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              v-model="Address"
              :rules="addressRules"
              label="Adresse"
              class="rounded-pill"
              required
              outlined
            ></v-text-field>
          </v-row>

           <v-row 
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              v-model="PostalCode"
              :rules="postal_codeRules"
              label="Code Postale"
              type="number"
              class="rounded-pill"
              required
              outlined
            ></v-text-field>
          </v-row>

          <v-row 
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              v-model="Email"
              :rules="emailRules"
              label="Email"
              class="rounded-pill"
              required
              outlined
            ></v-text-field>
          </v-row>
          <v-row 
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              :append-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
              :type="show ? 'text' : 'password'"
              v-model="Password"
              :rules="passwordRules"
              label="Mot de passe"
              class="rounded-pill"
              required
              outlined
              @click:append="show = !show"
            ></v-text-field>
          </v-row>
          <v-row 
            align="center"
            class="ml-2 mr-2"
          >
            <v-text-field
              :append-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
              :type="show ? 'text' : 'password'"
              v-model="ConfirmPassword"
              :rules="confirmpasswordRules"
              label="Confirmer Mot de passe"
              class="rounded-pill"
              required
              outlined
              @click:append="show = !show"
              ></v-text-field>
            </v-row>
            <v-row
              align="center"
              justify="center"
            >
              <v-btn
                color="success"
                class="mr-4 mb-5 rounded-pill"
                v-on:click="validate()"
              >
                Validate
              </v-btn>
            </v-row>
            <v-card-text>
              <v-row
                align="center"
                justify="center"
                class="mt-2"
              >
                <p>Déjà inscrit ? <a @click="back">Connectez-Vous</a></p>
            </v-row>
          </v-card-text>
          </v-form>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<style>
.reg_form {
    margin-left: 10px;
    margin-right: 10px;
}
.title{
    margin-left: 45%;
    margin-bottom: 15px;
}
</style>

<script>
export default {
  data(){
    return {
      Firstname: '',
      Lastname: '',
      Username: '',
      Email: '',
      Password: '',
      ConfirmPassword: '',
      show: false,
      
      firstnameRules: [
        v => !!v || 'First name is required'
      ],
      lastnameRules: [
        v => !!v || 'Last name is required'
      ],
      usernameRules: [
        v => !!v || 'Username is required',
      ],
      ageRules: [
        v => !!v || 'Age is required',
      ],
      addressRules: [
        v => !!v || 'Address is required'
      ],
      emailRules: [
        v => !!v || 'Email is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      passwordRules: [
        v => !!v || 'Password is required',
      ],
      confirmpasswordRules: [
        v => v === this.Password || 'Password is not the same'
      ],

    };
  },
  methods : {
    validate(){
      this.$router.push('login');
    },
    back() {
      this.$router.go(-1);
    }
  },
  layout : 'nolayout'
};
</script>