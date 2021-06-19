<template>
  <v-container>
    <v-card elevation="5">
      
      <v-app-bar color="secondary">
          <div style="font-size: 1.5rem">Assistant</div>
      </v-app-bar>

      <v-container>
        <v-app>

          <v-card>

            <v-app-bar>

              <v-app-bar-title>
                <div style="font-size:1.5rem">Chat</div>
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