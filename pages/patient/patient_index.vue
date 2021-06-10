<template>
  <v-app>

    <v-card height="80px">

      <v-row
      justify="center"
      >
        <div class="display-2 mt-3">Bienvenue {{user.fullName}}</div>
      </v-row>

      <v-row justify="center">
        <div class="subheading mt-1">Que pouvons nous faire pour vous aujourd'hui ?</div>
      </v-row>
    </v-card>

    <v-container fluid>

      <v-card class="mx-auto mt-10">

        <v-card-title class="display-1 font-weight-medium justify-center" >
          Dashboard
        </v-card-title>

        <v-container fluid>
          <v-row>

            <v-col align-self="left">

              <v-card class="mx-auto">
                <v-card-title class="font-weight-light">
                  Profile
                </v-card-title>
                <v-col>
                <v-avatar
                tile
                color="primary"
                size="90">
                  <span>{{user.initials}}</span>
                </v-avatar>
                </v-col>
                <v-card-text class="text-justify body-1 font-weight-bold">
                  NOM: {{user.fullName}},<br>
                  Email: {{user.email}},<br>
                  Sexe: {{user.sex}},<br>
                  ID: {{user.ID}} <br>
                </v-card-text>
              </v-card>

            </v-col>

            <v-col align-self="right">

              <v-card class="mx-auto" min-width="100px">
                <v-card-title class="font-weight-light">
                  Rendez-vous
                </v-card-title>
                <v-calendar-weekly>
                </v-calendar-weekly>
              </v-card>
              
            </v-col>
          </v-row>

          <v-row>
            <v-col align-self="center">
              <v-card>
                <v-card-title class="justify-center">
                  Assistant
                </v-card-title>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-container>


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
        sex: 'M',
        ID: '2662951',
      },
    };
  },
  layout : 'patient_layout'
};
</script>