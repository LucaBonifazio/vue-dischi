<template>
  <header>
    <div class="top_bar d-flex justify-content-between align-items-center px-4">
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png"
        alt="logo"
        class="img-fluid"
      >
      <!-- <font-awesome-icon icon="fa-brands fa-spotify" /> -->
      <AppSearch @change="onChange" />
    </div>
  </header>
</template>

<script>
import AppSearch from '@/components/AppSearch.vue';

export default {
  name: 'AppHeader',
  components: {
    AppSearch,
  },
  data: () => ({
    value: 'none',
  }),
  methods: {
    onChange(selectedValue) {
      this.$emit('change', selectedValue);
    },
  },
};
</script>

<style lang="scss" scoped>
  .top_bar {
    height: 10vh;
    background-color: #2E3A46;
  }

  img {
    width: 80px;
    height: 80px;
    &:hover {
      cursor: pointer;
      transform: scale(1.1);
      transition: transform 0.3s ease-in-out;
    }
  }
</style>
