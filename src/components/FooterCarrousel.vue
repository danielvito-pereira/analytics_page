<template>
  <div class="pricing-plans">
    <div class="texto">
        <h2 class="h2">Pricing Plans</h2>
        <p class="p">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Elementum nisi aliquetvolutpat pellentesque volutpat est. 
        </p>
      </div>   
    <div class="plans">
      <div class="stantard">
        <h2 class="h2">Starter</h2>
          <p class="p">up to 3 users</p>
          <span class="splitter"></span>
          <p class="sifra">$29</p>
          <p class="p">per month</p>
          <button>Order</button>
      </div>
      <div class="stantard -white">
        <h2 class="h2">Standard</h2>
        <p class="p">up to 20 users</p>
        <span class="splitter"></span>
        <p class="sifra">$99</p>
        <p class="p">per month</p>
        <button>Order</button>
      </div>
      <div class="stantard">
        <h2 class="h2">Premium</h2>
        <p class="p">up to 200 users</p>
        <span class="splitter"></span>
        <p class="sifra">$299</p>
        <p class="p">per month</p>
        <button>Order</button>
      </div>
    </div>

    <div class="ocultar">
      <swiper 
        :spaceBetween="30"
        :pagination="{
          clickable: true,
        }"
        :modules="modules"
        class="mySwiper"
      >
        <swiper-slide>
          <div class="stantard">
            <h2 class="h2">Starter</h2>
            <p class="p">up to 3 users</p>
            <span class="splitter"></span>
            <p class="sifra">$29</p>
            <p class="p">per month</p>
            <button>Order</button>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="stantard -white">
            <h2 class="h2">Standard</h2>
            <p class="p">up to 20 users</p>
            <span class="splitter"></span>
            <p class="sifra">$99</p>
            <p class="p">per month</p>
            <button>Order</button>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="stantard">
            <h2 class="h2">Premium</h2>
            <p class="p">up to 200 users</p>
            <span class="splitter"></span>
            <p class="sifra">$299</p>
            <p class="p">per month</p>
            <button>Order</button>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import 'swiper/scss';
import 'swiper/scss/navigation';


// import required modules
import { Pagination } from "swiper";
export default {
  
  name: 'FooterCarrousel',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },

}
</script>
<style lang="scss" scoped>
  .pricing-plans{
    width:90%;
    height: 656px;
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    justify-content: space-between;
    overflow: hidden;
    .texto{
      .h2{
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 700;
        font-size: 40px;
        line-height: 47px;
        text-align: center;
        color: #FFFFFF;
      }
      .p{
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 400;
        font-size: 18px;
        line-height: 150%;
        text-align: center;
        color: #8794BA;
      }

    }
    .plans{
      gap: 80px;
      width:90%;
      height: 440px;
      flex-flow: row nowrap;
      align-items: center;
      justify-content: center;
      @media screen and (max-width:882px) {
        display: none;
      }  
      @media screen and (min-width:882px) {
          display: flex;
          justify-content: space-evenly;
      }
      }
    }
    .stantard{
        width: 280px;
        height: 358px;
        background: #0F1F4B;
        border-radius: 30px;
        display: flex;
        flex-flow: column nowrap;
        align-items: center;
        justify-content: space-evenly;
        .h2{
          font-family: 'Roboto';
          font-style: normal;
          font-weight: 700;
          font-size: 25px;
          line-height: 29px;
          text-align: center;
          color: #FFFFFF;
        }
        .p {
          font-family: 'Roboto';
          font-style: normal;
          font-weight: 400;
          font-size: 13px;
          line-height: 140%;
          /* or 18px */

          text-align: center;

          /* text / secondary */

          color: #8794BA;
        }
        .sifra {
          font-family: 'Roboto';
          font-style: normal;
          font-weight: 700;
          font-size: 30px;
          line-height: 35px;
          text-align: center;
          color: #FFFFFF;
        }
      }
    .-white{
        background: #FFFFFF;
        .h2{

            color: #172755;
        }
        .sifra {
            color: #172755;
        }
    }
    .splitter{
      width: 220px;
      height: 1px;
      background: #2A407C;
    }
    .-blue{
      background-color:var(--blue-2);
      color: var(--white);
      .comment{
        border-bottom: 1px solid #fdfdfd;
      }
      .name{
        h1{
          color: var(--primary-color);
        }
        p{
          color: var(--white);
        }
      }
    }
    /*swiper */
    @media screen and (max-width: 825px){
        .TestimonialSection{
          .priceList{
            display: none;
          }
        }
        .ocultar{
          display: flex !important;
        } 
    }
    .ocultar{
      display: none;
    } 
    .mySwiper{
      width: 375px;
      margin-left: 100px;
    }
</style>

      

