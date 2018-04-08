<template>
  <div id="app">
    <div class="container">
      <three-wrapper />
      <title-card />
      <nav-links />
      <social-links />
    </div>
  </div>
</template>

<script>
import TitleCard from './components/TitleCard'
import NavLinks from './components/NavLinks'
import SocialLinks from './components/SocialLinks'
import ThreeWrapper from './components/ThreeWrapper/ThreeWrapper'

export default {
  name: 'App',
  components: {
    TitleCard,
    NavLinks,
    SocialLinks,
    ThreeWrapper
  }
}
</script>

<style lang='scss' scoped>
@import './assets/scss/index.scss';

#app {
  position: relative;
  display: block;
  width: 100%;
  height: 100%;
  background-color: $dark-bg;
}

.container {
  position: relative;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  width: 100%;
  height: 100%;
  max-width: 1200px;
  margin: 0 auto;
  background-color: $dark-bg;
}

</style>
