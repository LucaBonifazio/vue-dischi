<template>
  <div>
    <AppHeader />
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
};
</script>

<style lang="scss">
  @import "~bootstrap/scss/bootstrap";
  @import url('https://fonts.googleapis.com/css2?family=Lato&display=swap');

  body {
  font-family: 'Lato', sans-serif;
  }
</style>
