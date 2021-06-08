<template>
  <v-app>
    
    
    <v-parallax
    dark
    height="560"
    src="/images/fond.jpg"
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
          
          <v-btn
          class="green--text mt-3"
          dark
          rounded
          outlined
          elevation="5"
          >
            <NuxtLink to="/">Faites vous aider maintenant !</NuxtLink>
          </v-btn>
      
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
          src="/images/doctors.jpg"
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
          src="/images/doctors2.jpg"
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

    <v-carousel
    class="mt-10"
    height="550"
    cycle
    hide-delimiters
    >
      <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="slide-x-reverse-transition"
      transition="slide-x-transition"
      >
        <v-row
        class="fill-height"
        align="center"
        justify="center"
        >
          <v-col
          class="text-center"
          v-if="i == 0"
          >
            <div class="display-2 font-weight-thin"
            style="text-shadow: 0 0 8px black;"
            >
              Pas encore inscrit sur notre site ?
            </div>

            <div 
            class="subheading mt-2"
            style="color: white;text-shadow: 0 0 8px black;"
            >
              Inscrivez-vous et accédez à une aide médical d'exception.
            </div>
        
            <v-btn
            class="green--text mt-3"
            dark
            rounded
            elevation="5"
            >
            <NuxtLink to="/register">Faites le dés maintenant !</NuxtLink>
            </v-btn>
          </v-col>

          <v-col
          class="text-center"
          v-if="i == 1"
          >
          <div class="display-2 font-weight-thin"
            style="text-shadow: 0 0 8px black;"
            >
              Des questions, Des problémes, au sujet de votre santé ?
            </div>
            <div class="subheading mt-2"
            style="color: white;text-shadow: 0 0 8px black;">
              Une examination constituer de questions/réponses est là pour vous aider
            </div>
        
            <v-btn
            class="green--text mt-3"
            dark
            rounded
            elevation="5"
            >
            <NuxtLink to="/bot">Accéder a l'examination</NuxtLink>
            </v-btn>
          </v-col>

          <v-col
          class="text-center"
          v-if="i == 2"
          >
            <div 
            class="display-2 font-weight-thin"
            style="text-shadow: 0 0 5px black;"
            >
              Un doute sur ce que vous avez ? Vous ne savez ce que c'est ?
            </div>

            <div 
            class="subheading mt-2"
            style="color: white;text-shadow: 0 0 8px black;"
            >
              Contactez l'un de nos médecins, il vous aidera a trouver votre probléme dans le plus
              bref délai.
            </div>
        
            <v-btn
            class="green--text mt-3"
            dark
            rounded
            elevation="5"
            >
              <NuxtLink to="/">Contactez l'un de nos medecins !</NuxtLink>
            </v-btn>
            
          </v-col>

          <v-col
          class="text-center"
          v-if="i == 3"
          >
          
            <div 
            class="display-2 font-weight-thin"
            style="text-shadow: 0 0 5px black;"
            >
              Vous êtes l'un de nos medecins ?
            </div>

            <div 
            class="subheading mt-2"
            style="color: white;text-shadow: 0 0 8px black;"
            >
              Connectez-vous, accédez à votre profil et gérer votre agenda.
            </div>

            <v-btn
            class="green--text mt-3"
            dark
            rounded
            elevation="5"
            >
            <NuxtLink to="/doctor_login">Connectez-vous</NuxtLink>
          </v-btn>

        </v-col>
      </v-row>
      </v-carousel-item>
    </v-carousel>
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

<script>
export default {
  data () {
    return {
      items: [
        {
          src: '/images/connexion.jpg',
        },
        {
          src: '/images/question.jpg',
        },
        {
          src: '/images/doctors7.jpg',
        },
        {
          src: 'images/doctors8.jpg',
        },
      ],
    };
  },
};
</script>
