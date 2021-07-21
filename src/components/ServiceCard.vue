<template>
<!-- there are the 3 cards: img with text -->

    <div class="col-3 position-relative cardWrap">
        <div class="darkWrap">
            <img class="serv" :src="require('@/assets/img/' + details.img + '.jpg')" alt="Our provided services">
        </div>
        <!-- "text" -->
        <div class="wrapperTxt position-absolute">
            <img class="line position-absolute" :src="require('@/assets/img/' + details.line + '.svg')" alt="Just a line for beauty">
            <h3>{{details.h3}}</h3>
            <p>{{details.colorP}}</p>
        </div>

    </div>
</template>

<script>
export default {
  name: "ServiceCard",
  props:{
      details: Object
    },
};
</script>

<style lang="scss" scoped>

.cardWrap{
    top: -80px;
}

.darkWrap{
  filter: brightness(50%);

    .serv{
        width:350px;
        height:350px;
        overflow: hidden;
        border-end-end-radius: 10%;
    }

}

.wrapperTxt{
    top: 75%;
    left: 15%;
}

.line{
    width:3rem;
    height:2rem;
    top:-30px;
    
}

h3{
    font-weight:500;
    color:white;
}

p{
    color:yellow;
    font-size: 1.4rem;
}

</style>
