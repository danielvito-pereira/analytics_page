<template>
  <div class="nav">
    <HeaderLogo/>
    <HeaderNav/>
    <MenuButtons/>

  </div>
</template>

<script>
import HeaderLogo from "./HeaderLogo"
import MenuButtons from "./MenuButtons"
import  HeaderNav from "./HeaderNav"
export default {
  name:'HeaderMenu',
  components:{
    HeaderLogo,
    MenuButtons,
    HeaderNav,

  }
}
</script>

<style lang="scss">
  .nav{
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    justify-content: space-between;
    width: 90%;
    max-width: 120rem;
    top: 2rem;
    position: absolute;
    @media screen and (max-width:882px) {
      background: #172755;
      box-shadow: 0px 4px 4px #12214D;   
    }  
  }
</style>