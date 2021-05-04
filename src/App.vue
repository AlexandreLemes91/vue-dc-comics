<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';

export default {
  name: 'App',
  components: {
  Header,
  }
}
</script>

<style lang="scss">
body{
  padding: 0px;
  margin: 0px;
  box-sizing: border-box;
}

#app{
  display: flex;
  justify-content: center;
  font-family: 'Roboto Condensed', sans-serif;
}

.container {
  width: 1300px;
}
</style>
