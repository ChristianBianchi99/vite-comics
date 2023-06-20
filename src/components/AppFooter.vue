<script>
export default {

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
                                <li>
                                    link
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
  footer{
    background-color: pink
  }
  .top-bar{
    background-color: blue;
    height: 145px;
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