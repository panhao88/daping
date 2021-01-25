<template>
  <dv-border-box-8 style="width:100%;height:100%" >
    <div style="width: 100%; height: 100%;" ref="myCharts" ></div>
  </dv-border-box-8>
</template>

<script>
import linFen from "../assets/141000";
export default {
  name: "",
  // 接收父组件传递过来的参数
  props: {},
  // 注册组件
  components: {},
  // 定义变量
  data() {
    return {};
  },
  // 事件方法执行
  methods: {},
  // 页面初始化方法
  mounted() {
    const myCharts = this.$echarts.init(this.$refs.myCharts);
    var mapName = "临汾市";
    this.$echarts.registerMap(mapName, linFen);
    var options = {
      backgroundColor: "rgb(24,26,29)",
      grid: {
        x: 30,
        y: 0,
        x2: 30,
        y2: 20,
      },
      title: {
        x: "center",
        y: 10,
        text: mapName,
        textStyle: {
          color: "white",
        },
      },

      series: [
        {
          type: "map",
          mapType: mapName,
          label: {
            normal: {
              show: true,
              formatter: "{b}",
              position: "top",
              marginLeft: 10,
              rotate: 45,
            },
            emphasis: {
              textStyle: {
                color: "#fff",
              },
            },
          },
          itemStyle: {
            normal: {
              borderColor: "#389BB7",
              areaColor: "rgb(3,88,205)",
            },
            emphasis: {
              areaColor: "rgb(155,38,38)",
              borderWidth: 0,
            },
          },

          animation: false,
        },
      ],
    };
    myCharts.setOption(options);
  },
  // 监听值变化
  watch: {},
  // 计算
  computed: {},
};
</script>

<style scoped lang='scss'>
</style>
