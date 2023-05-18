<template>
  <div class="text">
    <h1 class="h1">
      Monitor your business on real-time dashboard
    </h1>
    <p class="p">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Elementum nisi aliquet volutpat pellentesque volutpat est. 
    </p>
  </div>
</template>

<script>

  export default {
    name: 'ContainerText',    
  }
</script>

<style lang="scss">
  .text{
    width: 100%;
    display: flex;
    flex-flow: column nowrap;
    gap: 20px;
    .h1{
      font-family: 'Roboto';
      font-style: normal;
      font-weight: 700;
      font-size: 1.8rem;
      line-height: 120%;
      color: #FFFFFF;
      @media screen and (max-width:350px) {
        font-size: 1.3rem;
      }
      @media screen and (min-width:882px) {
        width: 550px;
        font-size: 3.225rem;
      } 
    }
    .p{
      font-family: 'Roboto';
      font-style: normal;
      font-weight: 400;
      font-size: 1.5rem;
      line-height: 150%;
      color: #8794BA;
      @media screen and (max-width:350px) {
        font-size: 1rem;
      }
      @media screen and (min-width:882px) {
        width: 550px;
        font-size: 18px;
      } 
    }
  }
</style>