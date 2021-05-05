<template>
    <header>
        <div class="container">
            <a href=""><img :src="img.url" :alt="img.name"></a>
            <ul>
                <li v-for="(link, index) in links" :key="link.text + index"><a href="link.  url">{{link.text}}</a></li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',

    data(){
        return{
            img: {name:'dc-logo', url: require('@/assets/img/dc-logo.png'),},

            links: [
                {text: 'characters', url: "@"},
                {text: 'comics', url: "@"},
                {text: 'movies', url: "@"},
                {text: 'tv', url: "@"},
                {text: 'games', url: "@"},
                {text: 'collectibles', url: "@"},
                {text: 'videos', url: "@"},
                {text: 'fans', url: "@"},
                {text: 'news', url: "@"},
                {text: 'shop', url: "@"},
            ],
        }
    },
}
</script>

<style scoped lang="scss">
@import "./scss/general.scss";

.container{
    display: flex;
    align-items: center;
    justify-content: space-between;
}

img{
    max-width: 80px;
}

ul{
    display: flex;
}

ul li{
    padding: 40px 0;
    margin: 0 15px;
    border-top: 3px solid transparent;
    border-bottom: 3px solid transparent;
    transition: border-bottom-color 0.3s;
}

li a{
    color: $default-dark-color;
    text-decoration: none;
    font-size: 14px;
    text-transform: uppercase;
    font-weight: 700;
    transition: color 0.5s;
}

ul li:last-child{
    margin-right: 0pxs;
}

ul li:hover{
    border-bottom-color: $brand-color;
}

ul li:hover a{
    color: $brand-color;
}
</style>