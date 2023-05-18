<template>
  <div class="bottom">
    <FooterLogo/>
    <HeaderNav/>
    <FooterRedes/>
  </div>
</template>

<script>
  import FooterLogo from "./FooterLogo.vue"
  import HeaderNav from "./HeaderNav.vue"
  import FooterRedes from "./FooterRedes.vue"
  export default {
    name: 'FooterBottom',    
    components:{
      HeaderNav,
      FooterRedes,
      FooterLogo
    }
  }
</script>
<style lang="scss">
  .bottom{
    display: flex;
    width: 90%;
    max-width: 120rem;
    max-height: 94px;
    align-content: center;
    justify-content: space-between;
  }
</style>