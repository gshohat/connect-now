<script setup>
import { ref } from 'vue'
import VideoGame from "./VideoGame.vue";

let videoGames = ref({});
const getVideoGames = async() => {
  const res = await fetch('https://public.connectnow.org.uk/applicant-test/');
  videoGames.value = await res.json();
  console.log('videoGames', videoGames);
}

getVideoGames();

</script>

<template>

  <div v-for="videoGame in videoGames">
    <VideoGame :videoGame="videoGame" />
  </div>

</template>

<style scoped>
</style>
