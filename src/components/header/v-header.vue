<template>
  <div class="header">
    <div class="header-logo">
      <img :src="require('../../assets/img/logo.svg')" alt="logo"/>
    </div>
    <div class="header-nav">
      <div class="header-nav-icon">
        <img :src="require('../../assets/icons/icon1.svg')" alt='icon1'/>
      </div>
      <div class="header-nav-icon">
        <img :src="require('../../assets/icons/icon2.svg')" alt='icon2'/>
      </div>
      <div class="header-nav-icon">
        <img :src="require('../../assets/icons/icon3.svg')" alt='icon3'/>
      </div>
      <div class="header-nav-icon">
        <img :src="require('../../assets/icons/icon4.svg')" alt='icon4'/>
      </div>
      <div class="header-nav-icon">
        <img :src="require('../../assets/icons/icon5.svg')" alt='icon5'/>
      </div>
      <div class="header-nav-icon">
        <img :src="require('../../assets/icons/icon6.svg')" alt='icon6'/>
      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: 'v-header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    height: 60px;
    max-width: 1236px;
    margin: auto;
    margin: 0 auto;
    background: rgba(255, 255, 255, 0.6);
    backdrop-filter: blur(20px);
  }

  .header-logo {
    display: flex;
    align-items: center;
  }

  .header-nav {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .header-nav-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 59px;
  }
</style>
