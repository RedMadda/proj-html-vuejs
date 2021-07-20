<template>
    <section class="jumbo, container">
        <div class="row row-col-4 my-5">
            <span class="mt-5">Certified fitness professionals</span>
            <h1>Take control of your health</h1>
            <img src="../assets/img/yelloWave.png" alt="single wave icon">
            <p> Curabitur ipsum dolor sit amet consec adipisi elit rerum sic amet. </p>
            <div class="wrapper-btn">
                <button class="tubeBtn rounded-pill font-weight-bold my-3"><i class="bi bi-youtube"></i>&nbsp; Visit my YouTube channel</button>
                <button class="buyBtn rounded-pill ms-3">Buy Avada today  <i class="bi bi-arrow-right-short"></i></button>
            </div>
       </div>
    </section>
    
</template>

<script>

export default {
    name: "JumboText"
}
</script>

<style lang="scss" scoped>
@import "../style/mixins.scss";

.container{
    flex-direction: column;
    align-content: flex-start;
    color:white;

    span{
        color: #CD353D;
        font-weight: 500;
        font-size: 1.9rem;
    }

    h1{
        font-size: 4rem;
    }
    img{
        height:50px;
        width:200px;
    }
    p{
        font-size:1.4rem;
    }

    .tubeBtn{
        @include btn(15px 35px, none);
    }

    .buyBtn{
      @include btn(15px 35px, 2px solid rgb(75, 73, 78), black);

      i{
        font-size: 1.5rem;
        position: absolute;
        line-height: 0;
        }
    }
}

</style>