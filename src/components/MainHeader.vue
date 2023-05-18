<template>
  <header class="header">
      <HeaderMenu/>
      <HeaderNavAtivo/>
      <HeaderContainer/>
      
  </header>
</template>

<script>
import HeaderMenu from "./HeaderMenu"
import HeaderNavAtivo from "./HeaderNavAtivo.vue"
import HeaderContainer from "./HeaderContainer"
export default {
  name: 'MainHeader',
  components:{
    HeaderMenu,
    HeaderNavAtivo,
    HeaderContainer
  }
}
</script>


<style scoped lang="scss">
  .header{
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
    width: 100%;
    height:120vh;
    background-image: url(../assets/img/bk/background-top-mobile.png);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-color: #EEEEF7;
    margin-bottom: 3rem;
    @media screen and (min-width:882px) {
      background-image: url(../assets/img/bk/background-top\ \(2\).png);
      height:120vh !important;
    }

    @media screen and (min-width:530px) {
      height:150vh;
    }
  }
</style>
