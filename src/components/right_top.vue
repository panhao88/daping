<template>
  <dv-border-box-8>
    <div class="box">
      <div class="title">
        <div style="margin: 0.5rem 0 0 0.6rem">告警趋势</div>
      </div>
      <div class="content" ref="lineCharts">
      </div>
    </div>
  </dv-border-box-8>
</template>
<script>
  export default {
    name: "",
    // 接收父组件传递过来的参数
    props: {},
    // 注册组件
    components: {},
    // 定义变量
    data() {
      return {
        lineOption: {
          color:['rgb(255,185,128)','rgb(90,177,239)','rgb(253,34,216)', 'rgb(24,185,154)'],
          legend: {
            data: ['告警信息', '违规信息', '红头信息', '涉密信息'],
            textStyle: {
              color: '#fff'
            },
          },
          tooltip: {
            trigger: 'axis' 
          },
          textStyle: {
            color: '#fff'
          },
          grid: {
            left: '3%',
            right: '4%',
            bottom: '3%',
            containLabel: true
          },
          xAxis: {
            type: 'category',
            boundaryGap: false,
            data: ['1/1', '1/2', '1/3', '1/4', '1/5', '1/6', '1/7'],
            axisLine: {
              lineStyle: {
                color: '#fff'
              }
            }
          },
          yAxis: {
            type: 'value',
            axisLine: {
              lineStyle: {
                color: '#fff'
              }
            }
          },
          series: [
            {
              name: '告警信息',
              type: 'line',
              // stack: '总量',
              // smooth: true,
              data: [2820, 182, 191, 234, 290, 330, 310],
            },
            {
              name: '违规信息',
              type: 'line',
              // stack: '总量',
              // smooth: true,
              data: [1570, 2320, 2010, 1540, 1900, 3300, 4100],
              lineStyle: {
                color: 'rgb(90,177,239)'
              }
            },
            {
              name: '红头信息',
              type: 'line',
              // stack: '总量',
              // smooth: true,
              data: [3210, 3302, 3001, 3340, 3900, 3300, 3210],
            },
            {
              name: '涉密信息',
              type: 'line',
              // stack: '总量',
              // smooth: true,
              data: [2800, 1932, 1901, 1934, 1290, 1830, 1920],
            }
          ]
        }
      };
    },
    // 事件方法执行
    methods: {},
    // 页面初始化方法
    mounted() {
      const MyLine = this.$echarts.init(this.$refs.lineCharts)
      MyLine.setOption(this.lineOption)
    },
    // 监听值变化
    watch: {},
    // 计算
    computed: {},
  };
</script>

<style scoped lang='scss'>
  .box {
    width: 100%;
    height: 100%;
  }

  .title {
    color: white;
    font-size: 1.7rem;
    display: flex;
    height: 20%;
    width: 100%;
  }

  .content {
    height: 80%;
    width: 100%;
  }
</style>