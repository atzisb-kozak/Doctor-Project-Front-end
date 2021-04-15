<template>
  <v-app>
      <v-parallax
      dark
      height="525"
      src="/fond.jpg"
      jumbotron
    >
    <v-row
      align="center"
      justify="center"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        <h1 class="display-1 font-weight-thin mb-4">
          Bienvenue
        </h1>
        <h4 class="subheading" >
          Vous ne vous sentez pas bien ? 
          Consultez avec l'un de nos médecins !
        </h4>
      </v-col>
    </v-row>
  </v-parallax>
    <v-card
    class="mx-md-3 mt-md-3"
    elevation="2"
    max-width="500"
    outlined>
    <v-card-title>Qui sommes nous ?</v-card-title>
    <v-card-text>
      Nous sommes un groupe indépendants présentant des services médicaux au personnes dans le 
      besoin. Nous avons mis en place ce site sur lequel vous êtes actuellement pour permettre,
      a vous ou bien a d'autres de pouvoir accéder a tout moment au nombreux médecins afin de vous
      aider au mieux. 
    </v-card-text>
    <v-content>
    <v-img
      class="ml-auto"
      src="/doctors.jpg"
      max-height="250"
      max-width="500">
    </v-img>
    </v-content>
    </v-card>

  </v-app>
  
</template>

<style scoped>
h1{
  color: black;
}
h4{
  color: black;
}
</style>
