<template>
    <div class="comic">
        <img :src="details.thumb" :alt="details.series">
        <h2>{{details.series}}</h2>
    </div>
</template>

<script>
export default {
    name: 'ComicCard',
    props: ['details'],
}
</script>

<style scoped lang='scss'>
@import "./scss/general.scss";

.comic{
    width: calc( 100% / 6 - 20px);
    margin: 20px 10px;
    transition: 0.3s;
    &:hover{
        transform: scale(1.1);
    }

    img{
        height: 192px;
        width: 192px;
        object-fit: cover;
        object-position: top;
    }

    h2{
        color: white;
        font-size: 14px;
        text-transform: uppercase;
        font-weight: 400;
        margin: 15px 0;
        text-align: left;
    }

}

</style>