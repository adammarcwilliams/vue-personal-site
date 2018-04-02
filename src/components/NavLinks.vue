<template>
  <div class="nav-links">
    <div class="link link--about">about</div>
    <div class="link link--source">source code</div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>
@import '../assets/scss/index.scss';

.nav-links {
  position: absolute;
  top: 0;
  left: 0;
  display: block;
  width: 100%;
  height: 100%;
}

.link {
  position: absolute;
  display: block;
  font-family: $ptsans;
  font-size: 24px;
  color: $light-copy;
  padding-bottom: 5px;
  border-bottom: transparent solid 3px; // fixes hover movement on transformed link

  &:hover {
    border-bottom: $light-copy solid 3px;
  }
}

.link--about {
  top: 20px;
  left: 40px;
}

.link--source {
  bottom: 71px;
  right: -17px;
  transform: rotate(90deg);
}

</style>
