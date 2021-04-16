<template>
  <v-app>
    
    <v-parallax
    dark
    height="560"
    src="/fond.jpg"
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

    <v-main>

      <v-row>
      
        <v-col align-self="center">
        
          <v-card
          class="d-flex align-center mx-auto mt-4 "
          elevation="0"
          width="550"
          >
        
            <v-card-title>
              Qui sommes nous ?
            </v-card-title>

            <v-card-text class="d-flex justify-center mt-3">
              Nous sommes un groupe indépendants présentant des services médicaux 
              au personnes dans le besoin.
              Nous avons mis en place ce site sur lequel vous êtes actuellement pour permettre,
              à vous ou bien à d'autres de pouvoir accéder à tout moment au nombreux médecins de
              notre plateforme afin de vous aider au mieux. 
            </v-card-text>

          </v-card>
        </v-col>
    
        <v-col>
          
          <v-img
          
          class="ml-auto mt-8 align-center"
          src="/doctors.jpg"
          aspect-ratio="1.8"
          >
          </v-img>

        </v-col>
      </v-row>
    </v-main>

    <v-row>

      <v-col>

        <v-img
          class="mr-auto mt-10"
          src="/doctors2.jpg"
          max-height="400"
          max-width="600">
        </v-img>

      </v-col>

      <v-col align-self="center">
        
        <v-card
        class="d-flex align-center mt-5"
        width="550"
        elevation="0"
        >

          <v-card-title>
            Que faisons-nous ?
          </v-card-title>

          <v-card-text class="d-flex justify-center mt-3" >
            Nous apportons notre soutient de par ce site en proposant des aides aux personnes
            ayant des problémes medicales, Le site propose des rendez-vous avec des médecins
            ou encore une examination constituer de Questions/Réponses afin d'identifier votre
            probléme et trouver la meilleure approche pour vous.
          </v-card-text>

        </v-card>
      </v-col>
    </v-row>

    <v-parallax
    class="mt-9"
    height="560"
    src="/doctors3.jpg"
    >
    
      <v-row
      align="center"
      justify="center"
      >

        <v-col
        class="text-center"
        >
          <h1 class="display-1 font-weight-bold mb-4">
            Malade ? Vous ne savez pas ce que c'est ?
          </h1>
      
          <v-btn
          class="green--text"
          dark
          rounded
          outlined
          color="#00000"
          elevation="5"
          >
            Faites vous aider maintenant !
          </v-btn>
      
        </v-col>
      </v-row>

    </v-parallax>
  </v-app>
</template>

<style scoped>
h1{
  color: black;
}
.subheading{
  color:black;
}

</style>
