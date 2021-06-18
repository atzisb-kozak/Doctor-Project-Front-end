<template>
  <v-app >

    <v-container>

    <v-card>

      <v-card-title>
        Rendez-vous
      </v-card-title>

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
            Mettre un rendez-vous
          </v-btn>
            
        </v-app-bar>

        <v-sheet height="400px">
          <v-calendar
          v-model="focus"
          ref="calendar"
          type="week"
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
    }
  },
  layout : 'doctor_layout'
};

</script>

<style>

</style>