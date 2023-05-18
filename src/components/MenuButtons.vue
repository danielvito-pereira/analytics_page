<template>
  <div class="buttons">
    <HeaderBtn/>
  </div>
</template>

<script>
import HeaderBtn from "./HeaderBtn"
export default {
  name:'MenuButtons',
  components:{
    HeaderBtn
  }
}
</script>

<style lang="scss">
  .buttons{
    display: flex;
    flex-flow: row nowrap;
    gap: 1rem;
  }
</style>