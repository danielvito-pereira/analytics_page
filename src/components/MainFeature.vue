<template>
  <div class="feature">
    <div class="fel">
      <figure class="icon">
        <img src="../assets/img/Icon1.svg" alt="" srcset="">
      </figure>
      <div class="txts">
        <h3 class="h3">Monitoring 24/7</h3>
        <p class="p">
          Lorem ipsum dolor sit amet, conse ctetur adipis cing elit. Elementum nisi aliquet volutpat.
        </p>
      </div>
    </div>
    <div class="fel">
      <figure class="icon">
        <img src="../assets/img/Icon2.svg" alt="" srcset="">
      </figure>
      <div class="txts">
        <h3 class="h3">Widget System</h3>
        <p class="p">
          Sapien in etiam vitae nibh nunc mattis imperdiet sed nullam. Vitae et, tortor pulvinar risus pulvinar.
        </p>
      </div>
    </div>
    <div class="fel">
      <figure class="icon">
        <img src="../assets/img/Icon3.svg" alt="" srcset="">
      </figure>
      <div class="txts">
        <h3 class="h3">Best Performance</h3>
        <p class="p">
          Lorem ipsum dolor sit amet, consectetur adipis cing elit. Elementum nisi aliquet volutpat.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import MainFeature from "./MainFeature.vue"
import HeaderContainer from "./HeaderContainer"
export default {
  name: 'MainFeature',
  components:{

  }
}
</script>


<style scoped lang="scss">
  .feature{
    display: flex;
      flex-flow: column nowrap;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
      @media screen and (min-width:882px) {
          flex-flow: row nowrap;
      }
      @media screen and (min-width:530px) {
        align-items: stretch;
      }
    .fel{
      display: flex;
      gap: 20px;
      flex-flow: row nowrap;
      align-items: center;
      justify-content: space-between;
      @media screen and (min-width:882px) {
          flex-flow: column nowrap;
      }
  
      .icon{
        width: 15%;
        @media screen and (max-width:280px) {
          width: 25%;
        }
      }
      .txts{
        display: flex;
        flex-flow: column nowrap;
        gap: 10px;
        @media screen and (min-width:882px) {
          align-items: center;
          max-width: 380px;
        }
        .h3{
          font-family: 'Roboto';
          font-style: normal;
          font-weight: 700;
          font-size: 16px;
          line-height: 19px;
          color: #172755;
        }
        .p{
          font-family: 'Roboto';
          font-style: normal;
          font-weight: 400;
          font-size: 14px;
          line-height: 140%;
          color: #8794BA;
          min-width: 246px;
          @media screen and (min-width:882px) {
            max-width: 380px;
            text-align: center;
          }
        }
      }
    }
  }
</style>
