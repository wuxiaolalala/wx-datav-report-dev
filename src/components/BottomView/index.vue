<template>
  <div class="bottom-view">
    <!-- <ve-line :data="chartData" /> -->
  </div>
</template>

<script>
export default {
  name: 'BottomView',
  data () {
    return {
      chartData: {
        rows: [
          {
            日期: '1月1日',
            销售额: '4187'
          },
          {
            日期: '1月2日',
            销售额: '5187'
          },
          {
            日期: '1月3日',
            销售额: '6187'
          },
          {
            日期: '1月4日',
            销售额: '7187'
          },
          {
            日期: '1月5日',
            销售额: '8187'
          }
        ],
        columns: ['日期', '销售额']
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.bottom-view {
}
</style>
