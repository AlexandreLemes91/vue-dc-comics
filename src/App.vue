<template>
  <div id="app">
    <Header />

    <Banner />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Banner from '@/components/Banner.vue';

export default {
  name: 'App',
  components: {
  Header,
  Banner,
  }
}
</script>

<style lang="scss">
*{
  padding: 0px;
  margin: 0px;
  box-sizing: border-box;
}

#app{
  font-family: 'Roboto Condensed', sans-serif;
}

.container {
  margin: 0 auto;
  width: 1300px;
}
</style>
