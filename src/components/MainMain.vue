<template>
  <main class="main">
    <MainFeatures/>
    <MainReports/>
    <FooterMain/>
  </main>
</template>

<script>
import MainFeatures from "./MainFeatures"
import MainReports from "./MainReports"
import FooterMain from "./FooterMain"
export default {
  name: 'MainMain',
  components:{
    MainFeatures,
    MainReports,
    FooterMain
  }
}
</script>


<style scoped lang="scss">
    .main{
      width: 100%;
      display: flex;
      flex-flow: column nowrap;
      align-items: center;
      background-color: #EEEEF7;
      gap: 50px;
    }
</style>
