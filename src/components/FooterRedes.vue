<template>
  <div class="redes">
    <a href=""><img src="../assets/img/Facebook.png" alt="Facebook" srcset=""></a>
    <a href=""><img src="../assets/img/Twitter.png" alt="Twitter" srcset=""></a>
    <a href=""><img src="../assets/img/Instagram.png" alt="Instagram" srcset=""></a>
  </div>
</template>

<script>
  export default {
    name: 'FooterRedes ',    
  }
</script>

<style lang="scss">
  .redes{
    width: 100px;
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    justify-content: space-around;
    a{
      img{
        background-color: #172755;
      }
    }
  }
</style>