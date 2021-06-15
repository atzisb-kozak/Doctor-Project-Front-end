<template>
  <v-app>
    <v-container>
      <v-card class="mx-auto">

        <v-card-title class="font-weight-light">
          Profile
        </v-card-title>

        <v-col>

          <v-avatar
          tile
          color="primary"
          size="90"
          >

            <span>
              {{user.initials}}
            </span>

          </v-avatar>
        </v-col>

        <v-card-text class="text-justify body-1 font-weight-bold">
          NOM: {{user.fullName}},<br>
          Email: {{user.email}},<br>
          Sexe: {{user.sex}},<br>
          ID: {{user.ID}} <br>
        </v-card-text>

      </v-card>
    </v-container>
  </v-app>
</template>

<script>
export default {
  data: () => ({

    user:{
      initials: 'QS',
      fullName: 'Quentin SAM-LONG',
      email: 'test@test.com',
      sex: 'M',
      ID: '2662951',
    },
  }),
};
</script>