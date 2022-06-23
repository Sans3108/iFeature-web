<script setup>
import hover_link from './hover_link.vue';
</script>

<template>
  <div class="wrapper">
    <hover_link class="url" url="https://open.spotify.com/artist/1NkeIgGpORkhxCUluCnnFT" text="Spotify" underline/>
    <hover_link class="url" url="https://www.youtube.com/ifeature" text="YouTube" underline/>
    <hover_link class="url" url="https://www.instagram.com/ifeaturemusic" text="Instagram" underline/>
    <hover_link class="url" url="https://soundcloud.com/ifeature" text="SoundCloud" underline />
    <hover_link class="url" url="https://discord.com/invite/4znaQPa" text="Discord" underline />
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 10px;
  height: 80px;
  width: 100%;
  background-color: var(--background-color-soft);
  border-top-left-radius: 50px;
  border-top-right-radius: 50px;
  box-shadow: 0px 3px 15px rgba(0, 0, 0, 0.2);
}
</style>