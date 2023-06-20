<script>
export default {

}
</script>
<template lang="">
    <header>
        <div class="container h100">
            <div class="row h100">
                <div class="col">
                    <div class="logo">
                        Logo
                    </div>
                </div>
                <div class="col">
                    <div class="list">
                        <ul>
                            <li>
                                <a href="">Link</a>
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
  header{
    background-color: green;
    height: 100px;
  }
  .row{
    justify-content: space-between;
  }
</style>