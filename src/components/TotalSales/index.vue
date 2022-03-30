<template>
  <div class="total-sales">
    <common-card title="累计销售额" value="$ 3,566,78">
      <template>
        <div class="compare-wrapper">
          <div class="compare">
            <span>日同比</span>
            <span class="emphasis">7.33%</span>
            <div class="increase" />
          </div>
          <div class="compare">
            <span>月同比</span>
            <span class="emphasis">38.79%</span>
            <div class="decrease" />
          </div>
        </div>
      </template>
      <template v-slot:footer>
        <span>昨日销售额 </span>
        <span class="emphasis">$ 3,566,767</span>
      </template>
    </common-card>
  </div>
</template>

<script>
import commonCardMixins from '../../mixins/commonCardMixins'
export default {
  mixins: [commonCardMixins],
  data () {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.total-sales {
  .compare-wrapper {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    .compare {
      margin-top: 3px;
      font-size: 12px;
      display: flex;
      align-items: center;
    }
  }
}
</style>
