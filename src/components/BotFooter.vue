<template>
    <footer>
        <div class="container">
            <a class="btn" href="/">SIGN-UP NOW!</a>
            <div class="socials">
                <h2>{{socialsList.title}}</h2>
                <ul>
                    <li v-for="(social,index) in socialsList.socials" :key="social.name + index">
                        <a :href="social.link"><img :src="social.url" :alt="social.name"></a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'BotFooter',

    data(){
        return{
            socialsList:{
                title: 'follow us',
                socials: [
                    {name: 'facebook', url: require('@/assets/img/footer-facebook.png'), link: '/'},
                    {name: 'twitter', url: require('@/assets/img/footer-twitter.png'), link: '/'},
                    {name: 'youtube', url: require('@/assets/img/footer-youtube.png'), link: '/'},
                    {name: 'pinterest', url: require('@/assets/img/footer-pinterest.png'), link: '/'},
                    {name: 'periscope', url: require('@/assets/img/footer-periscope.png'), link: '/'},
                ]
            }
        }
    }
}
</script>

<style lang="scss" scoped>
@import "./scss/general.scss";

footer{
    background-color: $default-dark-color;
    padding: 30px;

    .container{
        display: flex;
        justify-content: space-between;
        align-items: center;

        .btn{
            text-decoration: none;
            color: white;
            padding: 10px;
            border: 3px solid $brand-color;
            transition: 0.3s, box-shadow 1.2s;
            &:hover{
                color: $brand-color;
                border-color: white;
                box-shadow: 20px 0px 25px white,
                            -20px 0px 25px white;

            }
        }

        .socials{
            display: flex;
            align-items: center;

            h2{
                color: $brand-color;
                text-transform: uppercase;
                margin-right: 20px;
            }

            ul{
                display: flex;

                li{
                    margin-left: 10px;
                    img{
                        transition: 0.25s;
                    }
                    &:hover img{
                        filter: brightness(300%);
                    }
                }
            }
        }
    }
}

</style>