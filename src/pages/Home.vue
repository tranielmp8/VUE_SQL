<template>
  <div class="home">
    <Hero />
    <DataList />
  </div>
</template>

<script>
import DataList from '../components/DataList.vue'
import Hero from '../components/Hero.vue';
  export default {
    components: {DataList, Hero},
    setup(){
      
    }
  }
</script>

<style scoped>

</style>