<template>
  <section class="quote">
    <QuoteContent v-for="(el,i) in content" :key="i" :details="el"/>
  </section>
</template>

<script>
import content  from "../data/QuoteInsp.js";
import QuoteContent from "../components/QuoteContent.vue";

export default {
    name: "Inspirational",
    components:{
      QuoteContent
    }, data(){
      return{
        content
      }
    }
}
</script>

<style lang="scss" scoped>

.quote{
    width: 100%;
    height: 113vh;
    background: linear-gradient(to bottom right, #0319EA  5%,  #A4063F 95%);
    
    
}

</style>