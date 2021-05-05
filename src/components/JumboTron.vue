<template>
  <section>
      <TopJumbo/>
      <BotJumbo/>
  </section>
</template>

<script>
import TopJumbo from '@/components/TopJumbo.vue';
import BotJumbo from '@/components/BotJumbo.vue';

export default {
    name: "JumboTron",
    components: {
        TopJumbo,
        BotJumbo,
    }
}
</script>

<style scoped lang="scss">
@import "./scss/general.scss";

</style>