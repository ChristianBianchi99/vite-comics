<script>
export default {
    data(){
        return{
            TopBarLinks:[
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
            ],
            MiddleBarLinks:[
                {
                    label: 'dc comics',
                    links: [
                        {
                            label: 'Characters',
                            link: '#'
                        },
                        {
                            label: 'Comics',
                            link: '#'
                        },
                        {
                            label: 'Movies',
                            link: '#'
                        },
                        {
                            label: 'TV',
                            link: '#'
                        },
                        {
                            label: 'Games',
                            link: '#'
                        },
                        {
                            label: 'Videos',
                            link: '#'
                        },
                        {
                            label: 'News',
                            link: '#'
                        },
                    ]
                },
                {
                    label: 'shop',
                    links: [
                        {
                            label: 'Shop DC',
                            link: '#'
                        },
                        {
                            label: 'Shop DC Collectibles',
                            link: '#'
                        },
                    ]
                },
                {
                    label: 'dc',
                    links: [
                        {
                            label: 'Terms of Use',
                            link: '#'
                        },
                        {
                            label: 'Privacy policy (New)',
                            link: '#'
                        },
                        {
                            label: 'Ad Choices',
                            link: '#'
                        },
                        {
                            label: 'Advertising',
                            link: '#'
                        },
                        {
                            label: 'Jobs',
                            link: '#'
                        },
                        {
                            label: 'Subscriptions',
                            link: '#'
                        },
                        {
                            label: 'Talent Workshops',
                            link: '#'
                        },
                        {
                            label: 'CPSC Certificates',
                            link: '#'
                        },
                        {
                            label: 'Ratings',
                            link: '#'
                        },
                        {
                            label: 'Shop Help',
                            link: '#'
                        },
                        {
                            label: 'Contact Us',
                            link: '#'
                        },
                    ]
                },
                {
                    label: 'sites',
                    links: [
                        {
                            label: 'DC',
                            link: '#'
                        },
                        {
                            label: 'MAD Magazine',
                            link: '#'
                        },
                        {
                            label: 'DC Kids',
                            link: '#'
                        },
                        {
                            label: 'DC Universe',
                            link: '#'
                        },
                        {
                            label: 'DC Power Visa',
                            link: '#'
                        },
                    ]
                },
            ],
            contacts:[
                {
                    label: 'Facebook',
                    icon: '/src/assets/footer-facebook.png',
                    link: '#'
                },
                {
                    label: 'Twitter',
                    icon: '/src/assets/footer-twitter.png',
                    link: '#'
                },
                {
                    label: 'You Tube',
                    icon: '/src/assets/footer-youtube.png',
                    link: '#'
                },
                {
                    label: 'Pinterest',
                    icon: '/src/assets/footer-pinterest.png',
                    link: '#'
                },
                {
                    label: 'Periscope',
                    icon: '/src/assets/footer-periscope.png',
                    link: '#'
                }
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
                                <li v-for="link in TopBarLinks" :key="index">
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
                        <div v-for="section in MiddleBarLinks" :key="index" class="section">
                            <h3>{{section.label}}</h3>
                            <ul>
                                <li v-for="link in section.links" :key="index">
                                    <a :href="link.link">
                                        {{link.label}}
                                    </a>
                                </li>
                            </ul>
                        </div>
                        <div class="bg-logo">

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
                            <button>Sign-up now!</button>
                        </div>
                    </div>
                    <div class="col">
                        <div class="follow-us">
                            follow us
                        </div>
                        <div class="contacts" v-for="contact in contacts" :key="index">
                            <a :href="contact.link">
                                <img :src="contact.icon" :alt="contact.label">
                            </a>
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
  .top-bar{
    background-color: $primary_color;
    padding: 40px 0;
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
    background-image: url('/src/assets/footer-bg.jpg');
    background-size: cover;
    padding: 30px 0;
    position: relative;
    .col{
        display: flex;
        flex-direction: column;
        max-height: 255px;
        flex-wrap: wrap;
    }
    .section{
        margin-right: 25px;
    }
    h3{
        text-transform: uppercase;
        font-size: 16px;
        color: white;
        margin-bottom: 10px;
    }
    ul{
        margin-bottom: 15px;
        a{
            font-size: 10px;
            color: gray;
            &:hover{
                color: lighten( gray, 30%);
            }
        }
    }
    .bg-logo{
        position: absolute;
        top: 0px;
        left: 52%;
        height: 100%;
        width: 470px;
        background-image: url('/src/assets/dc-logo-bg.png');
        background-size: 100%;
        background-position-y: 50%;
        background-position-x: 20%;
    }
  }
  .bottom-bar{
    background-color: rgb(48, 48, 48);
    padding: 20px 0;
    .row{
        justify-content: space-between;
    }
    .col{
        display: flex;
    }
    .follow-us{
        margin: 0 10px;
        text-transform: uppercase;
        color: $primary_color;
        font-weight: bold;
    }
    .follow-us, .contacts{
        display: flex;
        flex-wrap: wrap;
        align-content: center;
    }
    .sign-up{
        button{
            appearance: none;
            color: white;
            text-transform: uppercase;
            background-color: transparent;
            border: 2px solid $primary_color;
            padding: 10px;
        }
    }
    .contacts{
        a{
            margin: 0 10px;
            img{
                height: 30px;
            }
        }
    }
  }
</style>