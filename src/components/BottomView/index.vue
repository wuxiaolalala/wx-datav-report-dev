<template>
  <div class="bottom-view">
    <div class="view">
      <el-card shadow="hover">
        <template v-slot:header>
          <div class="title">关键词搜索</div>
        </template>
        <template>
          <div class="chart-wrapper">
            <div class="chart">
              <div class="chart-title">搜索用户数</div>
              <div class="chart-data">93,634</div>
              <v-chart :options="getSearchUserOptions()" />
            </div>
            <div class="chart">
              <div class="chart-title">搜索量</div>
              <div class="chart-data">198,782</div>
              <v-chart :options="getSearchNumberOptions()" />
            </div>
          </div>
          <div class="tabel-wrapper">
            <el-table :data="tableData">
              <el-table-column></el-table-column>
            </el-table>
            <el-pagination></el-pagination>
          </div>
        </template>
      </el-card>
    </div>
    <div class="view">
      <el-card shadow="hover">
        <template v-slot:header>
          <div class="title-wrapper">
            <div class="title">分类销售排行</div>
            <div class="radio-wrapper">
              <el-radio-group v-model="radioSelect" size="small">
                <el-radio-button label="品类"></el-radio-button>
                <el-radio-button label="商品"></el-radio-button>
              </el-radio-group>
            </div>
          </div>
        </template>
      </el-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BottomView',
  data () {
    return {
      radioSelect: '品类',
      tableData: []
    }
  },
  methods: {
    getSearchUserOptions () {
      return {
        xAxis: {},
        yAxis: {
          type: 'category'
        },
        series: [
          {
            type: 'bar'
          }
        ],
        grid: {
          top: 0,
          bottom: 0,
          left: 0,
          right: 0
        }
      }
    },
    getSearchNumberOptions () {
      return {
        xAxis: {},
        yAxis: {
          type: 'category'
        },
        series: [
          {
            type: 'bar'
          }
        ],
        grid: {
          left: 0,
          tio: 0,
          right: 0,
          bottom: 0
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.bottom-view {
  display: flex;
  .view {
    flex: 1;
  }
}
</style>
