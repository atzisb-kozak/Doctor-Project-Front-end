<template>
    <profile v-bind:user="{initials:'VS',username:'Chorizo',
    firstname:'Veronica',ID:'514696',age:'19',address:'91 rue de la deche',postal_code:'97391',
    email:'v.sanchez@gmail.com',password:'NACHOS',name: 'Sanchez'}"></profile>
</template>

<script>
import Profile from '../../components/profile_patient.vue';
export default {
  components:{
    Profile
  },
  layout : 'patient_layout'
};
</script>

<style>

</style>