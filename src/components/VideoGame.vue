<script setup>

const props = defineProps(['videoGame']);

const releaseDate = new Date(props.videoGame.first_release_date);

</script>

<template>
  <div class="video-game">
    <div class="description">
      <div class="title">{{videoGame.name}}</div>
      <div class="date">Release Date: {{releaseDate}}</div>
      <div>{{videoGame.summary}}</div>
    </div>

    <span class="rating">{{videoGame.rating}}</span>
  </div>

</template>

<style scoped>

.video-game {
  margin-bottom: 2%;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #0e192b;
}

.description {
  flex: 80%;
}

.title {
  font-weight: bold;
}

.date {
  margin-bottom: 1%;
}

.rating {
  flex: 20%;
  display: flex;
  justify-content: center;
}

</style>