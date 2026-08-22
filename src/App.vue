<script setup>
import PlaylistCard from './components/Playlist.vue'

const tiktokUrl = 'https://www.tiktok.com/@playlist_curator._'
</script>

<template>
  <header class="navbar">
    <div class="nav-container">
      <div class="nav-actions">
        <a :href="tiktokUrl" target="_blank" rel="noopener noreferrer" class="tiktok-btn" aria-label="TikTok Profile">
          <svg class="tiktok-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 640" width="16" height="16">
            <path fill="currentColor"
              d="M544.5 273.9C500.5 274 457.5 260.3 421.7 234.7L421.7 413.4C421.7 446.5 411.6 478.8 392.7 506C373.8 533.2 347.1 554 316.1 565.6C285.1 577.2 251.3 579.1 219.2 570.9C187.1 562.7 158.3 545 136.5 520.1C114.7 495.2 101.2 464.1 97.5 431.2C93.8 398.3 100.4 365.1 116.1 336C131.8 306.9 156.1 283.3 185.7 268.3C215.3 253.3 248.6 247.8 281.4 252.3L281.4 342.2C266.4 337.5 250.3 337.6 235.4 342.6C220.5 347.6 207.5 357.2 198.4 369.9C189.3 382.6 184.4 398 184.5 413.8C184.6 429.6 189.7 444.8 199 457.5C208.3 470.2 221.4 479.6 236.4 484.4C251.4 489.2 267.5 489.2 282.4 484.3C297.3 479.4 310.4 469.9 319.6 457.2C328.8 444.5 333.8 429.1 333.8 413.4L333.8 64L421.8 64C421.7 71.4 422.4 78.9 423.7 86.2C426.8 102.5 433.1 118.1 442.4 131.9C451.7 145.7 463.7 157.5 477.6 166.5C497.5 179.6 520.8 186.6 544.6 186.6L544.6 274z" />
          </svg>
          <span>Follow us on TikTok</span>
        </a>
      </div>
    </div>
  </header>

  <main class="container">
    <div class="playlist-grid">
      <PlaylistCard url="https://open.spotify.com/playlist/2ysqbdwrsxZQLLLRYlFvAC?si=0V0wA2B-T5OGINtJwkp0Ig" />
      <PlaylistCard url="https://open.spotify.com/playlist/6d8HW1ksDk9z1A926gLgbq?si=eoeOVVcwQU2kSdEdPU0erg" />
      <PlaylistCard url="https://open.spotify.com/playlist/3hzOnPQeEqHLOD8j6RF6yu?si=tGR0xUJDT2C1tZip0FIBNQ" />
      <PlaylistCard url="https://open.spotify.com/playlist/3FlLKMOQUIrCPrUrGqa36D?si=7AKnTgj3RbmD1uzyVlFg8w" />
      <PlaylistCard url="https://open.spotify.com/playlist/6n9OJktEHa7uyhdsscl3mZ?si=ICetGDtPTQ6qmfe7CJHUjg" />
    </div>
  </main>
</template>

<style>
body {
  margin: 0;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  background-color: #121212;
  color: #ffffff;
}

.navbar {
  background-color: #181818;
  border-bottom: 1px solid #282828;
  padding: 14px 0;
  position: sticky;
  top: 0;
  z-index: 100;
}

.tiktok-btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background-color: #ffffff;
  color: #000000;
  padding: 8px 18px;
  border-radius: 50px;
  text-decoration: none;
  font-size: 0.85rem;
  font-weight: 600;
  transition: opacity 0.2s, transform 0.2s;
}

.tiktok-btn:hover {
  opacity: 0.9;
  transform: scale(1.02);
}

.tiktok-icon {
  width: 16px;
  height: 16px;
  display: block;
}

.nav-container {
  width: 90%;
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 16px;
}

.container {
  width: 95%;
  max-width: 1600px;
  margin: 0 auto;
  padding: 40px 0;
}

.playlist-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 30px;
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
}

@media (max-width: 768px) {
  .nav-container {
    justify-content: center;
  }

  .playlist-grid {
    grid-template-columns: 1fr;
    max-width: 500px;
  }
}
</style>