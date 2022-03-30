<template>
  <div class="sasel-view">
    <v-chart :options="myoptions" />
  </div>
</template>

<script>
export default {
  name: 'SaselView',
  data () {
    return {
      myoptions: {
        xAxis: {
          // type: 'category'
        },
        yAxis: {},
        series: [
          {
            type: 'line',
            data: [100, 120, 249, 378]
          }
        ]
      }
    }
  },
  mounted () {
    // debugger
    // eslint-disable-next-line no-unused-expressions
    this.options
  }
}
</script>
<style lang="scss" scoped>
.sasel-view {
  width: 100%;
  height: 100%;
  .echarts {
    width: 100%;
    height: 100%;
  }
}
</style>
