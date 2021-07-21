<template>
<div class="cardWrap d-flex justify-content-center text-center">
  <div class="text-center ">
    <img class="icons mt-5" :src="require('@/assets/img/' + det.img)" >
    <h3 class="mt-4">{{det.h3}}</h3>
    <h2 class="mb-5">{{det.h2}}</h2>
    <p class="pTxt mb-5">{{det.p}}</p>
    <p>
      <a class="text-white" href="#">{{det.aTxt}} <i :class="'bi' + det.iGo"></i>
      </a>
    </p>
  </div>
</div>
</template>

<script>
export default {
  name: "AgainServCard",
  props: ["det"]
};
</script>

<style lang="scss" scoped>

.cardWrap{
  border: 3px solid #3240C1;
  height:100%;
  width: 25%;

  .icons{
    width: 40px;
    background-color: white;
    border-radius: 50%;
    padding: 10px;
  }

  h2{
    color: yellow;
    font-size:1rem;
    font-weight: 400;
  }

  .pTxt{
    width:70%;
    margin:auto;
  }

  a{
    font-weight:500;
  }

  i{
    background-color: rgba(49, 49, 49, 0.986);
    padding:4px;
    border-radius: 50%;
  }
}
</style>
