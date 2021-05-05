<template>
    <footer>
        <div class="container">
            <div class="link-list">
                <div v-for="(list, index) in linkList" :key="list.title + index">
                    <h4>{{list.title}}</h4>
                    <ul>
                        <li v-for="(link, ind) in list.links" :key="link.txt + ind">
                            <a :href="link.link">{{link.txt}}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="img-container">
                <img src="@/assets/img/dc-logo-bg.png" alt="dc-logo">
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'TopFooter',

    data(){
        return{
            linkList:[
                {title:'dc comics',
                links: [
                        {txt: 'characters', link: '/'},
                        {txt: 'comics', link: '/'},
                        {txt: 'movies', link: '/'},
                        {txt: 'TV', link: '/'},
                        {txt: 'Games', link: '/'},
                        {txt: 'Videos', link: '/'},
                        {txt: 'News', link: '/'},
                ]},
                {title:'shop',
                links: [
                        {txt: 'shop DC', link: '/'},
                        {txt: 'shop DC collectibles', link: '/'},
                ]},
                {title:'dc',
                links:[
                        {txt: 'term of use', link: '/'},
                        {txt: 'privacy policy (new)', link: '/'},
                        {txt: 'ad choices', link: '/'},
                        {txt: 'advertising', link: '/'},
                        {txt: 'jobs', link: '/'},
                        {txt: 'subscriptions', link: '/'},
                        {txt: 'talent workshops', link: '/'},
                        {txt: 'CPSC certificates', link: '/'},
                        {txt: 'ratings', link: '/'},
                        {txt: 'shop help', link: '/'},
                        {txt: 'contact us', link: '/'},
                ]},
                {title:'sites',
                links: [
                        {txt: 'DC', link: '/'},
                        {txt: 'MAD magazine', link: '/'},
                        {txt: 'DC kids', link: '/'},
                        {txt: 'DC universe', link: '/'},
                        {txt: 'DC power visa', link: '/'},
                ]},
            ],
        }
    }
}
</script>

<style scoped lang="scss">
    footer{
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: cover;
        height: 450px;
        overflow: hidden;
    }

    .container{
        display: flex;
        max-height: 100%;
        justify-content: space-between;
    }

    .link-list{
        display: flex;
        flex-direction: column;
        color: white;
        flex-wrap: wrap;
        padding: 40px 0;

        div{
            margin-right: 50px;
            margin-bottom: 20px;
        }

        h4{
            text-transform: uppercase;
            font-size: 24px;
            margin-bottom: 15px;
            }

        li:hover a{
            color: white;
        }

        a{  
            text-decoration: none;
            color: #888888;
            line-height: 1.5rem;
            text-transform: capitalize;
            transition: 0.3s;
        }
        
    }

    .img-container{
        flex-basis: 60%;
        position: relative;
        top: -100px;
    }
    img{
        width: 100%;
    }
</style>