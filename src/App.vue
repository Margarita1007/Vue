<template>
  <div class="wrapper">
    <vHeader/>
    <vHeaderNav/>
    <vMainWrapper/>
  </div>
</template>

<script>
import vHeader from './components/header/v-header.vue'
import vHeaderNav from './components/header/v-header-nav.vue'
import vMainWrapper from './components/main/v-main-wrapper.vue';


export default {
  name: 'App',
  components: {
    vHeader,
    vHeaderNav,
    vMainWrapper
  }
}
</script>

<style>
#app {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 22px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0;
  padding: 0;
}
</style>
