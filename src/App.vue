<template>
  <div>
    <AppHeader @change="onChange" />
    <AppMain />
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue';
import AppMain from '@/components/AppMain.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
  },
  props: {
    genre: String,
    selectedValue: String,
  },
  computed: {
    filteredProducts() {
      return this.products.filter((product) => product.type === this.selectedValue);
    },
  },
};
</script>

<style lang="scss">
  @import "~bootstrap/scss/bootstrap";
  @import url('https://fonts.googleapis.com/css2?family=Lato&display=swap');

  body {
  font-family: 'Lato', sans-serif;
  }
</style>
