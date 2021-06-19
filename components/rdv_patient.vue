<template>
  <v-app >

    <v-container>

    <v-card>

      <v-app-bar color="secondary">
        <div style="font-size: 1.5rem">Rendez-vous</div>
      </v-app-bar>

      <v-container>

        <v-app-bar elevation="1">

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

          <v-app-bar-title 
          v-if="$refs.calendar"
          >
            {{$refs.calendar.title}}
          </v-app-bar-title>

          <v-spacer></v-spacer>

          <v-btn>
            Demandez un Rendez-vous
          </v-btn>
            
        </v-app-bar>

        <v-sheet height="400px">
          <v-calendar
          v-model="focus"
          ref="calendar"
          type="week"
          :events="events"
          >
          </v-calendar>
        </v-sheet>
      </v-container>
    </v-card>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data:() => ({
    events:[
      {
        name: 'test',
        start:'2021-06-21 10:00',
        end:'2021-06-21 12:00',
      },
    ],
    focus:'',
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
    add(){
      
    }
  },
  layout : 'patient_layout'
};

</script>

<style>

</style>