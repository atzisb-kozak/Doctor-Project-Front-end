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

            <v-col>

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

            <v-col>

                <v-card>
                  <v-card-title>
                      Rendez-vous
                  </v-card-title>
                  <v-container>
                  <v-app-bar elevation="0">

                    <v-btn
                    fab
                    text
                    small
                    color="grey darken-2"
                    @click= prev
                    >
                      <v-icon small>
                        mdi-chevron-left
                      </v-icon>
                    </v-btn>

                    <v-btn
                    fab
                    text
                    small
                    color="grey darken-2"
                    @click= next
                    >
                      <v-icon small>
                        mdi-chevron-right
                      </v-icon>
                    </v-btn>

                    <v-app-bar-title v-if="$refs.calendar">
                      {{$refs.calendar.title}}
                    </v-app-bar-title>

                  </v-app-bar>

                  <v-sheet height="350px">
                    <v-calendar
                    v-model="focus"
                    ref="calendar"
                    type="week"
                    >
                    </v-calendar>
                  </v-sheet>
                  </v-container>

                </v-card>
            </v-col>
          </v-row>

          <v-row>
            <v-col>
              <v-card>
                <v-card-title class="justify-center">
                  Assistant
                </v-card-title>

              <v-container>
                <v-app>
                  <v-card>

                    <v-app-bar>
                      <v-app-bar-title>
                        Chat
                      </v-app-bar-title>
                    </v-app-bar>

                    
                    
                    <v-row justify="end">
                      <v-container>
                      <v-col>
                        <v-text-field
                        label="Message"
                        type="text"
                        clearable
                        clear-icon="mdi-close-circle"
                        append-outer-icon="mdi-send"
                        > 
                        </v-text-field>
                      </v-col>
                      </v-container>
                    </v-row>

                  </v-card>
                </v-app>
              </v-container>

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
  data: () => ({

    focus:'',

    user:{
      initials: 'QS',
      fullName: 'Quentin SAM-LONG',
      email: 'test@test.com',
      sex: 'M',
      ID: '2662951',
    },


    
  }),
  mounted () {
    this.$refs.calendar.move(1);
  },


  methods:{
    prev() {
      this.$refs.calendar.prev();
    },
    next(){
      this.$refs.calendar.next();
    },
  },
  layout : 'patient_layout'
};
</script>