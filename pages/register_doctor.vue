<template>
    <v-app>
        <v-main>
          <v-container fluid>
            <v-card 
            dark
            >
              <v-card-title class="title">
                  Inscription Docteur
              </v-card-title>
            <v-form class="reg_form"
            ref="form"
            v-model="valid"
            lazy-validation
            >

            <v-row>
                <v-col
                cols="12"
                md="4"
                >
                <v-text-field
                    v-model="Firstname"
                    :rules="firstnameRules"
                    label="Prénom"
                    required
                    outlined
                ></v-text-field>
                </v-col>

                <v-col
                cols="12"
                md="4"
                >
                <v-text-field
                    v-model="Lastname"
                    :rules="lastnameRules"
                    label="Nom"
                    required
                    outlined
                ></v-text-field>
                </v-col>

                <v-col
                cols="12"
                md="4"
                >
                <v-text-field
                    v-model="Username"
                    :rules="usernameRules"
                    label="Pseudo"
                    required
                    outlined
                ></v-text-field>
                </v-col>
            </v-row>

                <v-text-field
                    v-model="Email"
                    :rules="emailRules"
                    label="Email"
                    required
                    outlined
                
                    ></v-text-field>    

                    <v-text-field
                    v-model="Password"
                    :rules="passwordRules"
                    label="Mot de passe"
                    required
                    outlined
                    ></v-text-field>

                    <v-text-field
                    v-model="ConfirmPassword"
                    :rules="confirmpasswordRules"
                    label="Confirmer Mot de passe"
                    required
                    outlined
                    ></v-text-field>

                    <v-btn
                    color="success"
                    class="mr-4 mb-5"
                    v-on:click="validate()"
                    >
                    Validate
                    </v-btn>
            </v-form>
            </v-card>
          </v-container>
        </v-main>
    </v-app>

</template>

<style>
.reg_form{
    margin-left: 10px;
    margin-right: 10px;
}
.title{
    margin-left: 40%;
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
      
      firstnameRules: [
        v => !!v || 'First name is required'
      ],
      lastnameRules: [
        v => !!v || 'Last name is required'
      ],
      usernameRules: [
        v => !!v || 'Username is required',
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
    }
  }
};
</script>