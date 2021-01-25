<template>
  <dv-border-box-8>
    <div class="box">
      <div class="title">
        <div style="margin: 0.5rem 0 0 0.6rem">告警网站排名</div>
      </div>
      <div class="content">
        <dv-capsule-chart :config="config" style="width: 100%; height: 100%;" />
      </div>
    </div>
    <!--color: rgb(161, 203, 250)-->
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
      config: {
        data: [
          {
            name: "南阳",
            value: 90,
          },
          {
            name: "周口",
            value: 67,
          },
          {
            name: "漯河",
            value: 123,
          },
          {
            name: "郑州",
            value: 55,
          },
          {
            name: "西峡",
            value: 98,
          },
        ],
        shape: "roundRect",
        unit: "单位",
        showValue: true,
      },
    };
  },
  // 事件方法执行
  methods: {},
  // 页面初始化方法
  mounted() {},
  // 监听值变化
  watch: {},
  // 计算
  computed: {},
};
</script>

<style scoped lang='scss'>
//边框内的盒子 存放所有
.box {
  width: 100%;
  height: 100%;
  //   border: 1px solid red;
}
.title {
  color: white;
  font-size: 1.7rem;
  display: flex;
  height: 20%;
//   border: 1px solid red;
}

.content {
  height: 80%;
//   border: 1px solid pink;
}
</style>