<script>
export default {

}
</script>
<template lang="">
    <main>
        <div class="container h100">
            <div class="row h100">
                <div class="col">
                    <div class="contents">
                        --&gt Content goes here &lt--
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>
<style lang="scss" scoped>
  @use '../style/generals.scss' as *;
  main{
    background-color: black;
    height: 120px;
  }
  .contents{
    color: white;
    font-weight: bold;
    font-size: 20px;
  }
</style>