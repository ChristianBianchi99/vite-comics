<script>
export default {
    data(){
        return{
            links:[
                {
                    icon: '/src/assets/buy-comics-digital-comics.png',
                    label: 'digital comics',
                    link: '#',
                },
                {
                    icon: '/src/assets/buy-comics-merchandise.png',
                    label: 'dc merchandise',
                    link: '#',
                },
                {
                    icon: '/src/assets/buy-comics-subscriptions.png',
                    label: 'subscription',
                    link: '#',
                },
                {
                    icon: '/src/assets/buy-comics-shop-locator.png',
                    label: 'comic shop locator',
                    link: '#',
                },
                {
                    icon: '/src/assets/buy-dc-power-visa.svg',
                    label: 'dc power visa',
                    link: '#',
                },
            ]
        }
    }
}
</script>
<template lang="">
    <footer>
        <div class="top-bar">
            <div class="container h100">
                <div class="row h100">
                    <div class="col">
                        <div class="list">
                            <ul>
                                <li v-for="link in links" :key="index">
                                    <div class="icon">
                                        <img :src="link.icon" :alt="link.label">
                                    </div>
                                    <a :href="link.link">
                                        {{link.label}}
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="middle-bar">
            <div class="container h100">
                <div class="row h100">
                    <div class="col">
                        <div class="dc-comics">
                            <h3>DC COMICS</h3>
                            <ul>
                                <li>
                                    <a href="">
                                        link
                                    </a>
                                </li>
                            </ul>
                        </div>
                        <div class="shop">
                            <h3>SHOP</h3>
                            <ul>
                                <li>
                                    <a href="">
                                        link
                                    </a>
                                </li>
                            </ul>
                        </div>
                        <div class="dc">
                            <h3>DC</h3>
                            <ul>
                                <li>
                                    <a href="">
                                        link
                                    </a>
                                </li>
                            </ul>
                        </div>
                        <div class="sites">
                            <h3>SITES</h3>
                            <ul>
                                <li>
                                    <a href="">
                                        link
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="bottom-bar">
            <div class="container h100">
                <div class="row h100">
                    <div class="col">
                        <div class="sign-up">
                            sign up
                        </div>
                    </div>
                    <div class="col">
                        <div class="follow-us">
                            follow us
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
  @use '../style/generals.scss' as *;
  @use '../style/partials/_variables.scss' as *;
  footer{
    background-color: pink
  }
  .top-bar{
    background-color: $primary_color;
    padding: 40px;
    .col, .list, .ul{
        width: 100%;
    }
    ul{
        display: flex;
        justify-content: space-around;
        li{
            display: flex;
            flex-wrap: wrap;
            align-content: center;
            .icon{
                height: 45px;
            }
            a{
                display: flex;
                flex-wrap: wrap;
                align-content: center;
                text-decoration: none;
                color: white;
                text-transform: uppercase;
                margin-left: 10px;
                font-size: 10px;
            }
        }
        li:last-child .icon{
            height: 30px;
        }
    }
  }
  .middle-bar{
    background-color: lightblue;
    height: 250px;
  }
  .bottom-bar{
    background-color: violet;
    height: 100px;

    .row{
        justify-content: space-between;
    }
  }
</style>