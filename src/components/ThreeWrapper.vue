<template>
  <canvas id="canvas" />
</template>

<script>
require('../assets/js/three-app')

export default {
  name: 'ThreeWrapper',
  data () {
    return {
      x: null,
      y: null,
      audioSrc: null
    }
  }
}
</script>

<style scoped>
#canvas {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
