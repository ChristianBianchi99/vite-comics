<script>
import dcComics from '../data/dc-comics.js';
import Comics from './AppComics.vue';
export default {
  components:{
    Comics
  },
  data(){
    return{
      dcComics
    }
  }
}
</script>
<template lang="">
    <main>
      <div class="jumbotron">
      </div>
      <div class="background">
        <div class="container h100">
            <div class="row h100">
                <div class="col">
                    <div class="contents">
                      <div class="comics">
                        <Comics class="card" v-for="(comic, index) in dcComics" :key="index" :comic="comic" />
                      </div>
                      <button>
                        load more
                      </button>
                      <div class="badge">
                        current series
                      </div>
                    </div>
                </div>
            </div>
        </div>
      </div>
    </main>
</template>
<style lang="scss" scoped>
  @use '../style/generals.scss' as *;
  @use '../style/partials/_variables.scss' as *;
  .jumbotron{
    background-image: url('../assets/jumbotron.jpg');
    background-size: cover;
    height: 320px;
  }
  .background{
    background-color: rgb(28, 28, 28);
  }
  .container{
    position: relative;
  }
  .contents{
    color: white;
    font-weight: bold;
    font-size: 20px;
    padding: 40px 0 20px 0;
    display: flex;
    flex-direction: column;
    .comics{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      .card{
        width: calc(100% / 6 - 15px);
        margin-bottom: 40px;
      }
    }
    button{
      align-self: center;
      appearance: none;
      text-transform: uppercase;
      color: white;
      background-color: $primary_color;
      border: none;
      padding: 10px 50px;
      font-size: 10px;
    }
    .badge{
      text-transform: uppercase;
      color: white;
      background-color: $primary_color;
      padding: 10px 20px;
      position: absolute;
      top: -21.5px;
      left: -15px;
    }
  }
</style>