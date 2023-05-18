<template>
  <div class="shots">
    <div
      class="texto"
      v-for="(item, index) in dados"
      :key="item.id"
      :class="{'classe-especifica': index === 1}"
    >
      <div class="content">
        <h2 class="h2">{{ item.titulo }}</h2>
        <p class="p">{{ item.texto }}</p>
      </div>
      <!--
      <img src="../assets/img/screen-1.png" alt="" srcset="">
      -->
      <img :src="item.imagem" :alt="item.alt" />
    </div>
  </div>
</template>

<script>
  import screen1 from '../assets/img/screen-1.png';
  import screen2 from '../assets/img/screen-2.png';
  import screen3 from '../assets/img/screen-3.png';
export default {
  name: 'MainReports',
  data() {
    return {
      dados: [
        {
          id: 1,
          titulo: 'Automated Reports & Widget Alerts',
          texto:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Elementum nisi aliquet volutpat pellentesque volutpat est. Sapien in etiam vitae nibh nunc mattis imperdiet sed nullam. Vitae et, tortor pulvinar risus pulvinar sit amet.',
          imagem: screen1,
          alt: 'Imagem 1',
        },
        {
          id: 2,
          titulo: 'Fully customizable to address your needs',
          texto:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Elementum nisi aliquet volutpat pellentesque volutpat est. Sapien in etiam vitae nibh nunc mattis imperdiet sed nullam. Vitae et, tortor pulvinar risus pulvinar sit amet.',
          imagem: screen2,
          alt: 'Imagem 2',
        },
        {
          id: 3,
          titulo: 'Pre-built Dashboard Templates',
          texto:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Elementum nisi aliquet volutpat pellentesque volutpat est. Sapien in etiam vitae nibh nunc mattis imperdiet sed nullam. Vitae et, tortor pulvinar risus pulvinar sit amet.',
          imagem: screen3,
          alt: 'Imagem 3',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.shots {
  width: 100%;
  max-width: 120rem;
  padding: 1rem;
  display: flex;
  flex-flow: column nowrap;
  gap: 130px;
  margin-top: 3rem;

  .texto.classe-especifica {
    @media screen and (min-width: 882px) {
      flex-flow: row-reverse nowrap;
    }
  }

  .texto {
    display: flex;
    flex-flow: column nowrap;
    gap: 50px;
    align-items: center;

    @media screen and (min-width: 882px) {
      display: flex;
      flex-flow: column nowrap;
      gap: 50px;
      flex-direction: row;
      justify-content: space-evenly;
      align-items: center;
    }

    img {
      max-width: 600px;
      min-width: 250px;
    }
    .content {
      max-width: 480px;
      display: flex;
      flex-flow: column nowrap;
      gap: 30px;
      .h2 {
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 700;
        font-size: 27px;
        line-height: 35px;
        color: #172755;
        @media screen and (min-width: 882px) {
          font-size: 40px;
          line-height: 47px;
        }
      }
      .p {
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 400;
        font-size: 14px;
        line-height: 140%;
        color: #8794ba;
        @media screen and (min-width: 882px) {
          font-size: 18px;
          line-height: 150%;
        }
      }
    }
  }
}
</style>