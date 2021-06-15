<template>
  <v-container>
    <v-card elevation="5">

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
  </v-container>
</template>