<template>
  <div id="app">
    <Header/>
    <Albums/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Albums from './components/Albums.vue';


export default {
  name: 'App',
  components: {
    Header,
    Albums,
    
  }
}
</script>

<style lang="scss">
@import './src/assets/style/common';
@import './src/assets/style/variables';
</style>
