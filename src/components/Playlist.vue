<script setup>
defineProps({
  url: String
})

const getEmbedUrl = (url) => {
  const id = url.split('playlist/')[1]?.split('?')[0] || url
  return `https://open.spotify.com/embed/playlist/${id}?utm_source=generator&theme=0`
}
</script>

<template>
  <div class="card">
    <iframe
      :src="getEmbedUrl(url)"
      width="100%"
      height="500" frameborder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
      loading="lazy"
      style="border-radius: 12px;"
    ></iframe>

    <a :href="url" target="_blank" class="spotify-btn">
      Listen on Spotify
    </a>
  </div>
</template>

<style scoped>
.card {
  background-color: #1e1e1e;
  padding: 24px;
  border-radius: 16px;
  flex: 1;
  min-width: 0;
  width: 100%;
  box-sizing: border-box;
  text-align: center;
}

.spotify-btn {
  display: inline-block;
  margin-top: 15px;
  padding: 10px 20px;
  background-color: #1db954;
  color: white;
  text-decoration: none;
  font-weight: bold;
  border-radius: 50px;
  transition: transform 0.2s, background-color 0.2s;
}

.spotify-btn:hover {
  background-color: #1ed760;
  transform: scale(1.03);
}
</style>