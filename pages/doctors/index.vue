<template>
  <v-app>
    <v-main>
    <v-card height="80px" elevation="2">

        <v-row
        justify="center"
        >
          <div class="display-2">Bienvenue {{user.fullname}}</div>
        </v-row>

        <v-row justify="center">
          <div class="subheading">Quoi de neuf docteur ?</div>
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
              <profile></profile>
              </v-col>

              <v-col>
              <rdv></rdv>
              </v-col>

            </v-row>

            <v-row>

              <v-col>
                
              </v-col>

            </v-row>
            
          </v-container>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Profile from '../../components/profile_doc.vue';
import rdv from '../../components/rdv_doc.vue';
export default {
  components:{
    Profile,
    rdv,
  },
  data:() =>  ({
    user: {
      fullname: 'SAM-LONG Quentin'
    },
  }),
  layout: 'doctor_layout',
};
  
</script>
