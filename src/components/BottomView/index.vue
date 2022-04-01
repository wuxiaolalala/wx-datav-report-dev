<template>
  <div class="bottom-view">
    <div class="view">
      <el-card shadow="hover">
        <template v-slot:header>
          <div class="title-wrapper">关键词搜索</div>
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
        <template>
          <v-chart :options="getCategoryOptions()" />
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
    getCategoryOptions () {
      return {
        xAxis: {
          type: 'category'
        },
        yAxis: {},
        series: [
          {
            type: 'bar'
          }
        ],
        grid: {
          top: 0,
          bottom: 0,
          right: 0,
          left: 0
        }
      }
    },
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
  margin-top: 20px;
  .view {
    flex: 1;
    width: 50%;
    box-sizing: border-box;
    bo &:first-child {
      padding: 0 10px 0 0;
    }
    &:last-child {
      padding: 0 0 0 10px;
    }
    .title-wrapper {
      display: flex;
      align-items: center;
      height: 60px;
      box-sizing: border-box;
      border-bottom: 1px solid #eee;
      font-size: 14px;
      font-weight: 500;
      padding: 0 0 0 20px;
      .radio-wrapper {
        flex: 1;
        display: flex;
        justify-content: flex-end;
        padding-right: 20px;
      }
    }
  }
}
</style>
