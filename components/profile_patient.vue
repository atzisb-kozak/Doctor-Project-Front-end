<template>
  <v-app>
    <v-container>
      <v-card class="mx-auto"
      elevation="3">

        <v-app-bar color="secondary">
            <div style="font-size: 1.5rem">Profile</div>
        </v-app-bar>

        <v-divider ></v-divider>
        
        <v-container class="mt-3" fluid>
          <v-row justify="center">

            <v-avatar
            tile
            color="primary"
            size="90"
            >

              <span>
                {{user.initials}}
              </span>

            </v-avatar>
          </v-row>
        </v-container>
        
        <v-row>
          <v-col>

            <v-container>

              <v-card elevation="2">

                <v-card-title>Identité</v-card-title>

                <v-card-text class="text-justify body-1 font-weight-bold">
                  N° Sécurité Sociale: {{user.ID}} <br>
                  Nom: {{user.name}} <br>
                  Prénom: {{user.firstname}} <br>
                  Age: {{user.age}} <br>
                </v-card-text>

              </v-card>
            </v-container>
          </v-col>

          <v-col>

            <v-container>

              <v-card elevation="2">

                <v-card-title>Localisation</v-card-title>

                <v-card-text class="text-justify body-1 font-weight-bold">
                  Adresse: {{user.address}} <br>
                  Code Postal: {{user.postal_code}} <br>
                </v-card-text>

              </v-card>
            </v-container>
          </v-col>
        </v-row>

        <v-row>

          <v-col>

            <v-container>

              <v-card elevation="2">

                <v-card-title>Compte</v-card-title>

                <v-card-text class="text-justify body-1 font-weight-bold">
                Pseudo: {{user.username}} <br>
                Email: {{user.email}} <br>
                Mot de passe : {{user.password}} <br>
                </v-card-text>

              </v-card>
            </v-container>
          </v-col>
        </v-row>

      </v-card>
    </v-container>
  </v-app>
</template>

<script>
export default {
  props:{
    user: {
      type:Object,
      default: () => ({})
    }
  },

};
</script>