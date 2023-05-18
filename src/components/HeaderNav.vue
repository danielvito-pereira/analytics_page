<template>
  <nav class="navigation">
    <ul class="ul">
      <li><a href="">Products</a></li>
      <li><a href="">Pricing</a></li>
      <li><a href="">FAQ</a></li>
      <li><a href="">Blog</a></li>
    </ul>
  </nav>
</template>

<script>

export default {
  name:'HeaderNav',

}
</script>

<style lang="scss">
  .navigation{
    display: flex;
    flex-flow: row nowrap;
    .ul{
      display: flex;
      flex-flow: row nowrap;
      align-items: center;
      padding: 0px;
      gap: 36px;
      @media screen and (max-width:882px) {
        display: none;
      }
      li{
        a{
          color:#8794BA;
          &:hover{
            color: #465B95;
          }
        }
      }
    }
  }
</style>