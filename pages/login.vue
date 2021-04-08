<template>
    <v-app>
        <v-main>
            <v-card>
                <v-card-title class="title">
                    Login
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
        </v-main>
    </v-app>

</template>

<style>
.log_form{
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