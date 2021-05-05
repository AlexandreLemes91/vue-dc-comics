<template>
  <div id="app">
    <Header />

    <Banner />

    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Banner from '@/components/Banner.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'App',
  components: {
  Header,
  Banner,
  Footer,
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

li{
  list-style: none;
}
</style>
