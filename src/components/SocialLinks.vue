<template>
  <div class="social-links">
    <a href="https://twitter.com/amwcodes" class="link link--twitter" />
    <a href="https://github.com/adammarcwilliams" class="link link--github" />
    <a href="https://codepen.io/adammarcwilliams" class="link link--codepen"></a>
  </div>
</template>

<script>
export default {

}
</script>

<style lang='scss' scoped>

.social-links {
  position: absolute;
  bottom: 20px;
  left: 40px;
  width: 150px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.link {
  display: inline-block;
  width: 35px;
  height: 35px;
  background: no-repeat contain center;
}

.link--twitter {
  background-image: url('../assets/svg/twitter.svg');
}

.link--github {
  background-image: url('../assets/svg/github.svg');
}

.link--codepen {
  background-image: url('../assets/svg/codepen.svg');
}

</style>
