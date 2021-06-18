<template>
  <v-app>
    <profile></profile>
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