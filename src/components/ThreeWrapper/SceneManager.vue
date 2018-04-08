<template>
  <canvas class="SceneManager">
    <slot></slot>
  </canvas>
</template>

<script>
import * as THREE from 'three'

export default {
  name: 'SceneManager',
  data () {
    return {
      scene: new THREE.Scene(),
      width: null,
      height: null
    }
  },
  provide () {
    const global = {
      scene: this.scene
    }
    return {
      global
    }
  },
  mounted () {
    this.width = this.$el.offsetWidth
    this.height = this.$el.offsetHeight
    this.aspect = this.width / this.height
    this.camera = new THREE.PerspectiveCamera(75, this.aspect, 1, 1000)
    this.camera.position.z = 5

    this.renderer = new THREE.WebGLRenderer({
      alpha: true,
      antialias: false,
      canvas: this.$el
    })
    this.renderer.setPixelRatio(window.devicePixelRatio)
    this.renderer.setSize(this.width, this.height)

    // Start the render loop
    this.loop()
  },
  methods: {
    loop () {
      this.$children.forEach(child => {
        if (child.loop) child.loop()
      })
      this.renderer.render(this.scene, this.camera)
      requestAnimationFrame(this.loop)
    }
  }
}
</script>

<style scoped>
.SceneManager {
  position: relative;
  width: 100%;
  height: 100%;
}
</style>
