<template>
  <v-app>
    <v-main>
      <v-card height="80px" elevation="2" color="secondary">

        <v-row
        justify="center"
        >
          <div class="display-2">Bienvenue {{user.fullName}}</div>
        </v-row>

        <v-row justify="center">
          <div class="subheading">Que pouvons nous faire pour vous aujourd'hui ?</div>
        </v-row>
      </v-card>

      <v-container fluid>

        <v-card class="" elevation="5">

          <v-card-title class="display-1 font-weight-medium justify-center" >
            Dashboard
          </v-card-title>
          <v-col cols="15">
          <v-divider></v-divider>
          </v-col>
          <v-container fluid>

            <v-row>

              <v-col>
              <profile  v-bind:user="{
              initials:'VS',
              name: 'Sanchez',
              firstname:'Veronica',
              username:'Chorizo',
              ID:'514696',
              age:'19',
              address:'91 rue de la deche',
              postal_code:'97391',
              email:'v.sanchez@gmail.com',
              password:'NACHOS'}"
              ></profile>
              </v-col>

              <v-col>
              <rdv></rdv>
              </v-col>

            </v-row>

            <v-row>

              <v-col>
                <assistant></assistant>
              </v-col>

            </v-row>
            
          </v-container>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import profile from '../../components/profile_patient.vue';
import rdv from '../../components/rdv_patient.vue';
import assistant from '../../components/assistant.vue';

export default {
  components:{
    rdv,
    profile,
    assistant
  },
  data: () => ({

    user:{
      initials: 'QS',
      fullName: 'Quentin SAM-LONG',
      email: 'test@test.com',
      sex: 'M',
      ID: '2662951',
    },
  }),
  layout : 'patient_layout'
};
</script>