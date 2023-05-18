<template>
  <div class="main-screem">
    <img :src="imagemUrl" :alt="altText"> <!-- Exibe a imagem com base na URL e texto alternativo definidos nas propriedades computadas -->
  </div>
</template>

<script>
import pequena from '../assets/img/bk/Frame.png';
import grande from '../assets/img/bk/main-screenm.png';
export default {
  name: 'ContainerBanner',
  data() {
    return {
      imagemUrlPequena: pequena, 
      imagemUrlGrande:  grande, 
      tamanhoTelaPequeno: false // Inicialmente, considera a tela como não pequena
    };
  },
  mounted() {
    this.atualizarTamanhoTela(); // Atualiza o tamanho da tela quando o componente é montado

    // Adiciona um ouvinte de evento para redimensionamento da janela
    window.addEventListener('resize', this.atualizarTamanhoTela);
  },
  beforeDestroy() {
    // Remove o ouvinte de evento para redimensionamento da janela ao destruir o componente
    window.removeEventListener('resize', this.atualizarTamanhoTela);
  },
  methods: {
    atualizarTamanhoTela() {
      this.tamanhoTelaPequeno = window.innerWidth < 884; // Atualiza a propriedade tamanhoTelaPequeno com base na largura da janela
    }
  },
  computed: {
    imagemUrl() {
      return this.tamanhoTelaPequeno ? this.imagemUrlPequena : this.imagemUrlGrande; // Retorna a URL da imagem com base no tamanho da tela
    },
    altText() {
      return this.tamanhoTelaPequeno ? 'Imagem Pequena' : 'Imagem Grande'; // Retorna o texto alternativo da imagem com base no tamanho da tela
    }
  }
};
</script>

<style lang="scss">
.main-screem {
  width: 100%;
  background-color: #fff;
  border-radius: 8px;
  overflow: hidden;
  @media screen and (min-width:882px) {
    background-color: transparent;
    position: relative;  
    right: 0;
    left: 5.5%;
    bottom: -85px;
  } 
}
</style>
