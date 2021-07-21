<template>
  <div class="wrapperExt">
    <h2 class="text-white">{{details.quote}}</h2>
    <img class="line" :src="require('@/assets/img/' + details.lineNam)" alt="Just another yellow line. We really like them.">
    <!-- quote's author's infos -->
    <div class="authInfos align-items-center justify-content-center">
        <img :src="require('@/assets/img/' + details.imgAuth)" alt="Author profile pic">
        <span class="px-3 text-white">{{details.authName}}</span>
        <span class="city">{{details.homTown}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name:"QuoteContent",
  props:{
    details: Object
  }

}
</script>

<style lang="scss" scoped>
.wrapperExt{

  width:55%;
  margin:auto;
  text-align: center;
  padding-top:26%;

  h2{
    line-height: 1.3;
    font-size: 2.5rem;
    font-weight:500
  }

  .line{
    width: 75px;
    height:40px;
  }
}

.authInfos{
  display:flex;

  img{
    width:45px;
    border-radius:50%;
  }

  .city{
    color: #bd6c98a4
  }
}
</style>