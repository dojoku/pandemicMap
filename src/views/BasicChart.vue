<template>
  <div class="chart">
    <div id="mychart1" style="width:100%;height: 300px"></div>
  </div>
</template>

<script>
import echarts from 'echarts'  //引入echarts
export default {
  data () {
    return {
      mychart: ''
    }
  },
  mounted () {
    this.init()
  },
  methods: {
    init () {
      const myecharts = echarts.init(document.getElementById('mychart1'));
      var option = {
        title: {
          text: 'ECharts 入门示例'
        },
        tooltip: {},
        legend: {
          data: ['销量']
        },
        xAxis: {
          data: ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"]
        },
        yAxis: {},
        series: [{
          name: '销量',
          type: 'bar',
          data: [5, 20, 36, 10, 10, 20]
        }]
      }
      // 使用刚指定的配置项和数据显示图表。
      myecharts.setOption(option);
    }
  }
}
</script>

<style lang="scss" scoped>
</style>