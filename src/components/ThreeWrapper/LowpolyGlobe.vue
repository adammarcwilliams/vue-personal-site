<script>
import * as THREE from 'three'

export default {
  name: 'LowpolyGlobe',
  inject: ['global'],
  data () {
    return {
      speed: 0.01
    }
  },
  mounted () {
    this.geometry = new THREE.IcosahedronGeometry(1, 1)
    this.material = new THREE.MeshPhongMaterial({ color: 0x2194ce, flatShading: true })
    this.mesh = new THREE.Mesh(this.geometry, this.material)
    this.global.scene.add(this.mesh)
  },
  methods: {
    loop () {
      console.log('Object 3D recieved tick')
      this.mesh.rotation.y += this.speed
    }
  },
  render: h => h()
}
</script>
