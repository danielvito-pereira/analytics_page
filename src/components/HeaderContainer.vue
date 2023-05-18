<template>
    <div class="container">
      <ContainerBanner/>
      <ContainerText/>
    </div>
</template>

<script>
  import ContainerBanner from "./ContainerBanner"
  import ContainerText from "./ContainerText"
  export default {
    name:'HeaderContainer',
    components : {
      ContainerBanner,
      ContainerText
    },

  }
</script>

<style lang="scss">
  .container{
    width: 90%;
    max-width: 120rem;
    display:flex;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
    gap: 1.625rem;
    
    @media screen and (min-width:882px) {
      flex-flow: row-reverse nowrap;
    } 
  }
</style>