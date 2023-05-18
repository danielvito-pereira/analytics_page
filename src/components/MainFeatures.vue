<template>
  <div class="features">
    <div class="h2">Main Features</div>
    <p class="p">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Elementum nisi aliquet volutpat pellentesque volutpat est. Sapien in etiam vitae nibh nunc mattis imperdiet sed nullam. Vitae et, tortor pulvinar risus pulvinar sit amet. Id vel in nam malesuada.
    </p>
    <MainFeature/>
  </div>
</template>

<script>
import MainFeature from "./MainFeature.vue"
import HeaderContainer from "./HeaderContainer"
export default {
  name: 'MainFeatures',
  components:{
    MainFeature
  }
}
</script>


<style scoped lang="scss">
  .features{
    width: 90%;
    max-width: 120rem;
    display: flex;
    flex-flow: column nowrap;
    gap: 50px;
    margin-top: 3rem;
    margin-bottom: 3rem;
    @media screen and (min-width:882px) {
      align-items: center;
    }
    .h2{
      font-family: 'Roboto';
      font-style: normal;
      font-weight: 700;
      font-size: 30px;
      line-height: 35px;
      color: #172755;
    }
    .p{
      font-family: 'Roboto';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 140%;
      color: #8794BA;
      @media screen and (min-width:882px) {
        max-width: 1060px;
        text-align: center;
      }
    }
  }
</style>
