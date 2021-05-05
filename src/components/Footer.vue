<template>
    <footer>
        <TopFooter />
        <BotFooter />
    </footer>
</template>

<script>
import TopFooter from '@/components/TopFooter.vue';
import BotFooter from '@/components/BotFooter.vue';

export default {
    name: "Footer",
    components: {
        TopFooter,
        BotFooter,
    }
}
</script>

<style scoped lang="scss">

</style>