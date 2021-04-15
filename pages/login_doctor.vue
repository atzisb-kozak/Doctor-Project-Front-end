<template>
    <v-app>
        <v-main>
          <v-container fluid>
            <v-card class="card" dark > 
                <v-card-title class="title">
                    Log in Doctor
                </v-card-title>
            <v-form class="log_form"
            ref="form"
            v-model="valid"
            lazy-validation
            >
                <v-text-field
                    v-model="Username"
                    :rules="usernameRules"
                    label="Username"
                    required
                    outlined
                
                    ></v-text-field>    

                    <v-text-field
                    v-model="Password"
                    :rules="passwordRules"
                    label="Password"
                    required
                    outlined
                    ></v-text-field>

                    <v-btn
                    :disabled="!valid"
                    color="success"
                    class="mr-4"
                    @click="validate"
                    >
                    Validate
                    </v-btn>
            </v-form>
            <v-card-text>
            <p>Not registered yet ? <nuxt-link to="/register">Register here</nuxt-link></p>
            </v-card-text>
            </v-card>
          </v-container>
        </v-main>
    </v-app>

</template>

<style scoped>

.log_form {
  margin-left: 1rem;
  margin-right: 1rem;
}

.title {
  margin-left: 36%;
  margin-bottom: 1.2rem;
}

.card {
  width: 500px;
  margin-left: 32.5%;
  margin-top: 8%;
}

</style>

<script>
export default {
  data: () => ({

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
  }
};
</script>