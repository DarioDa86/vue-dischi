<template>
  <div id="app">
    <Header @optionChanged="onOptionChange"/>
    <Albums :optionSelected="optionSelected"/>
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
  },
  data() {
    return {
      optionSelected: ""
    }
  },
  methods: {
    // option viene automaticamente passata dall'evento (payload)
    onOptionChange(option) {
      this.optionSelected = option;
    }
  }
}
</script>

<style lang="scss">
@import './src/assets/style/common';
@import './src/assets/style/variables';
</style>
