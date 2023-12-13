<template>

   <h1 class="personal">Personal info</h1>

   <div v-for="job in jobs" :key="job.id">

      <router-link :to="{name: 'personal',params:{id: job.id}}">

       <label>{{ job.name }}</label>

      </router-link>

      

   </div>

</template>

<script>

import axios from "axios";

export default {
   data() {
      return {
         jobs : []
      }
   },
   mounted(){
      axios.get('http://localhost:3000/jobs').then(data => this.jobs = data.data)
   }
}
</script>

<style>

</style>