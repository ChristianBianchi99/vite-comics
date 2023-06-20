<script>
export default {
    data(){
        return{
            links:[
                {
                    label: 'characters',
                    active: false,
                    link: '#'
                },
                {
                    label: 'comics',
                    active: true,
                    link: '#'
                },
                {
                    label: 'movies',
                    active: false,
                    link: '#'
                },
                {
                    label: 'tv',
                    active: false,
                    link: '#'
                },
                {
                    label: 'games',
                    active: false,
                    link: '#'
                },
                {
                    label: 'collectibles',
                    active: false,
                    link: '#'
                },
                {
                    label: 'videos',
                    active: false,
                    link: '#'
                },
                {
                    label: 'fans',
                    active: false,
                    link: '#'
                },
                {
                    label: 'news',
                    active: false,
                    link: '#'
                },
                {
                    label: 'shop',
                    active: false,
                    link: '#'
                },
            ]
        }
    },
    methods:{
        becomeActive(index){
            for(let i=0; i<this.links.length; i++){
                this.links[i].active= false
            }
            this.links[index].active= true;
        }
    }
}
</script>
<template lang="">
    <header>
        <div class="container h100">
            <div class="row h100">
                <div class="col">
                    <div class="logo">
                        <img src="../assets/dc-logo.png" alt="Logo">
                    </div>
                </div>
                <div class="col">
                    <div class="list">
                        <ul>
                            <li v-for="(link, index) in links" :key="index" @click="becomeActive(index)">
                                <a :href="link.link" :class="link.active===true ? 'active' : ''">{{link.label}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
  @use '../style/generals.scss' as *;
  @use '../style/partials/_variables.scss' as *;
  header{
    padding: 15px 0;
  }
  .row{
    justify-content: space-between;
  }
  .col{
    display: flex;
    flex-wrap: wrap;
    align-content: center;
  }
  .logo{
    height: 65px;
  }
  .list{
    vertical-align: middle;
    text-transform: uppercase;
    font-size: 10px;
    font-weight: bold;
    ul{
        display: flex;
        li{
            margin: 15px;
            a{
                color: black;
                position: relative;
            }
            a.active{
                color: $primary_color;
            }
            a.active::after{
                content: '';
                position: absolute;
                height: 5px;
                width: 100%;
                background-color: $primary_color;
                left: 0;
                bottom: -42px;
            }
        }
    }
  }
</style>