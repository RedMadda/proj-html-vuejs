<template>
  <header>
    <!-- nav -->
    <div class="container">
        <!-- logo -->
        <a href="#"><img src="../assets/img/logo-mobile-2x.png" alt="Logo Avada Fitness" /></a>
        <!-- navbar link dynamic -->
        <nav>
            <ul>
                <li>
                    <a href="#" v-for="(link, index) in Links" :key="index" :class="{ active: link.activated }">{{ link.text }}</a>
                    <span>new </span>
                </li>
            </ul>

            <!-- button -->
            <button class="button rounded-pill mx-5">Schedule a workout</button>
            <i class="bi bi-cart"></i>
            <i class="bi bi-search"></i>
        </nav>
        <!-- /nav -->

    </div>
    <!-- /top/header -->
    <!-- jumbo -->
    <div class="container-fluid">
        <JumboText />
    </div>
    
  </header>
</template>

<script>
import Links from "../data/LinksHeader.js";
import JumboText from "@/components/JumboText.vue";

export default {
    name: "Header",
    components:{
        JumboText
    },
    data() {
        return {
          Links
        };
  },
};
</script>

<style lang="scss" scoped>

@import "../style/var.scss";
@import "../style/mixins.scss";

header{
    background-color: black;
    height: 89vh;
    position: relative;
}

.container {
    height: 90px;
    display: flex;
    justify-content: space-between;
    align-items: center;

// top-header start

    img{
        width:70%;
    }

    nav{
        display:flex;
        align-items: center;
    }

    ul {
      display: flex;
      height: 100%;
      margin-bottom:0;

        li {
            list-style-type: none;

            a {
                font-size: 1.1rem;
                font-weight: 500;
                text-decoration: none;
                padding: 10px;
                color: #C5C5C5;

                &.active{
                    color: white;
                }

               &:not(.active){
                    background: linear-gradient(to right,#C5C5C5,     white 50%,  #C5C5C5 50%);
                    background-clip: text;
                    -webkit-background-clip: text;
                    -webkit-text-fill-color: transparent;
                    background-size: 200% 100%;
                    background-position: 100%;
                    transition: background-position 275ms ease;
                    text-decoration: none;

                     &:hover {
                       background-position: 0 100%;
                    }

                }

            }
        }

        span{
            font-size: 0.8rem;
            background-color: #FFF941;
            padding:5px;
            border-radius: 3px;
        }

    }

    .button{
        @include btn(10px, none)
    }

    i{
        color:#C5C5C5;
        margin-right:2.5rem;
        cursor: pointer;
        font-size: 1.2rem;
    }
}
//end top-header, beginn jumbotron

.container-fluid{
  height: calc(89vh - 90px);
  background-image:  linear-gradient(to right, black 35%, transparent),
    url('~@/assets/img/slider82x-scaled.jpg');
  background-size: 100%;
}

</style>
