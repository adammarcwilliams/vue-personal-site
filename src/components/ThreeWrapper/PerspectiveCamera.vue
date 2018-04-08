<script>
import * as THREE from 'three'

export default {
  name: 'directionalLight',
  inject: ['global'],
  mounted () {
    this.light = new THREE.DirectionalLight(0xffffff, 1)
    this.global.scene.add(this.light)
  },
  render: h => h()
}
</script>
