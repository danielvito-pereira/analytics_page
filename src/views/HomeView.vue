<template>
    <MainHeader/>
    <MainMain/>
</template>

<script>
// @ is an alias to /src
import MainHeader from '@/components/MainHeader.vue'
import MainMain from '@/components/MainMain.vue'
export default {
  name: 'HomeView',
  components: {
    MainHeader,
    MainMain
  }
}
</script>
