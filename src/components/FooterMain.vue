<template>
  <footer class="footer">
    <div class="cont">
      <FooterCarrousel/>
      <FooterBottom/>
    </div>
  </footer>
</template>

<script>
  import FooterCarrousel from "./FooterCarrousel.vue"
  import FooterBottom from "./FooterBottom.vue"
  export default {
    name: 'FooterMain',    
    components:{
      FooterCarrousel,
      FooterBottom
    }
  }
</script>

<style lang="scss">
  .footer{
    width: 100%;
    height: 150vh;
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: flex-end;
    background-image: url(../assets/img/bk/background-bottom\ \(1\).png);
    background-repeat: no-repeat;
    background-size: cover;
    box-sizing: border-box;
    .cont{
      width: 100%;
      max-width: 120rem;
      height:80%;
      display: flex;
      flex-flow: column nowrap;
      align-items:center;
      justify-content: space-around;
    }
  }
</style>