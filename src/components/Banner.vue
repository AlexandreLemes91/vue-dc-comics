<template>
  <section>
        <div class="container">
            <ul>
                <li v-for="(img, index) in imgs" :key="img.name + index">
                    <a href="img.link">
                        <img :src="img.url" :alt="img.name">
                        <h2>{{img.name}}</h2>
                    </a>
                </li>
            </ul>
        </div>
  </section>
</template>

<script>
export default {
    name: "Banner",

    data(){
        return{
            imgs: [
                {
                    name: 'digital comics',
                    url: require('@/assets/img/buy-comics-digital-comics.png'),
                    link: '/',
                },
                {
                    name: 'merchandise',
                    url: require('@/assets/img/buy-comics-merchandise.png'),
                    link: '/',
                },
                {
                    name: 'subsciptions',
                    url: require('@/assets/img/buy-comics-subscriptions.png'),
                    link: '/',
                },
                {
                    name: 'comic shop locator',
                    url: require('@/assets/img/buy-comics-shop-locator.png'),
                    link: '/',
                },
                {
                    name: 'dc power visa',
                    url: require('@/assets/img/buy-dc-power-visa.svg'),
                    link: '/',
                },
                ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "./scss/general.scss";

    section{
        padding: 50px 0;
        background-color: $brand-color;
    }

    ul{
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    a{
        display: flex;
        align-items: center;
        color: white;
        text-transform: uppercase;
        text-decoration: none;
        transition: 0.2s;
        &:hover{
            transform: scale(1.03);
        }
        img{
            width: 55px;
            height: 55px;
            object-fit: contain;
        }

        h2{
            font-size: 14px;
            font-weight: 400;
            margin-left: 15px;
        }
    }

</style>