<template>
  <header>
    <div class="top_bar">
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png"
        alt="logo"
        class="img-fluid"
      >
    </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
};
</script>

<style lang="scss" scoped>
  .top_bar {
    height: 10vh;
    background-color: #2E3A46;
  }

  img {
    width: 100px;
    height: 100px;
    margin-top: 15px;
    margin-left: 20px;
    &:hover {
      cursor: pointer;
      transform: scale(1.1);
      transition: transform 0.3s ease-in-out;
    }
  }
</style>
