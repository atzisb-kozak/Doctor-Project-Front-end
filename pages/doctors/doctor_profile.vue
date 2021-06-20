<template>
  <v-app>
    <profile 
    v-bind:user="{
      initials:'MM',
      name:'Martin',
      firstname:'Matin',
      spec:'Proctologue',
      username:'Tarte tatin',
      email:'m.matin@gmail.com',
      password:'PommePoiré',
      }"
    >
    </profile>
  </v-app>
</template>

<script>
import profile from '../../components/profile_doc.vue';
export default {
  components:{
    profile,
  },
  data:() => ({

  }), 
  layout : 'doctor_layout'
};
</script>

<style>

</style>