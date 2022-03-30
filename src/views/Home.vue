<template>
  <div class="home">
    <top-view></top-view>
    <sasel-view></sasel-view>
    <bottom-view></bottom-view>
    <map-view></map-view>
  </div>
</template>

<script>
import TopView from '../components/TopView'
import SaselView from '../components/SaselView'
import BottomView from '../components/BottomView'
import MapView from '../components/MapView'
export default {
  name: 'Home',
  components: { TopView, SaselView, BottomView, MapView },
  data () {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.home {
  width: 100%;
  height: 100%;
  padding: 20px;
  background-color: #eee;
  box-sizing: border-box;
}
</style>
