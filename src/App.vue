<template>
  <div id="app">
    <div class="details">
      <div class="name">Adam Marc Williams</div>
      <div class="job-title">Interactive Developer</div>
      <div class="company">@rhythm.digital</div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',
  components: {
    HelloWorld
  }
};
</script>

<style lang='scss' scoped>
@import './utils/scss/index.scss';

#app {
  position: relative;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  width: 100%;
  height: 100%;
  background-color: $dark-bg;
}

.details {
  position: relative;
  width: 290px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-end;
  color: $light-copy;
  font-family: $ptsans;
  margin-right: 10vw;
}

.name {
  font-family: $oswald;
  font-size: 30px;
}

.job-title {
  font-size: 24px;
  margin-top: 5px;
}

.company {
  font-size: 20px;
  margin-top: 5px;
}


</style>
