<template>
  <main class="d-flex p-1">
    <div
      v-if="arrAlbums"
      class="row row-cols-sm-2 row-cols-md-3 row-cols-lg-6 g-3 container"
    >
      <AppMainCard
        v-for="album in arrAlbums"
        :key="album.i"
        :poster="album.poster"
        :title="album.title"
        :author="album.author"
        :year="album.year"
      />
    </div>
    <div
      v-else
      class="text-white"
    >
      Loading, page is not ready...
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import AppMainCard from '@/components/AppMainCard.vue';

export default {
  name: 'AppMain',
  components: {
    AppMainCard,
  },
  data() {
    return {
      arrAlbums: null,
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },
  created() {
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        this.arrAlbums = axiosResponse.data.response;
      });
  },
};
</script>

<style lang="scss" scoped>
  main {
    height: 90vh;
    background-color: #1E2D3B;
    overflow: auto;
    .container {
      display: flex;
      justify-content: center;
      align-items: inherit;
      margin: auto;
    }
  }
</style>
