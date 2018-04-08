<template>
  <div class="ThreeWrapper">
    <scene-manager>
      <lowpoly-globe />
      <directional-light />
    </scene-manager>
  </div>
</template>

<script>
import SceneManager from './SceneManager'
import LowpolyGlobe from './LowpolyGlobe'
import DirectionalLight from './DirectionalLight'

export default {
  name: 'ThreeWrapper',
  components: {
    SceneManager,
    LowpolyGlobe,
    DirectionalLight
  }
}
</script>

<style scoped>
.ThreeWrapper {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
