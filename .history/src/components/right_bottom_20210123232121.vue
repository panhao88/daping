<template>
  <div style="width: 100%; height: 100%">
    <div style="height: 50%">
      <dv-border-box-13>
        <div class="content">
          <div class="title">
            <div style="margin: 0.9rem 0 0 0.6rem">预警数据类型占比</div>
          </div>
          <!-- 饼图 -->
          <div ref="pie" style="width: 100%;height: 80%;"> </div>

        </div>
      </dv-border-box-13>
    </div>
    <div style="height: 50%; width: 100%">
      <dv-border-box-12>
        <div class="content">
          <div class="title">
            <div style="margin: 0.9rem 0 0 0.6rem">预警热点区/县</div>
          </div>
          <!-- 条形图 -->
          <div style="height: 80%" ref="charts"></div>
        </div>
      </dv-border-box-12>
    </div>
  </div>
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
        pieOption: {
          legend: {
            orient: 'vertical',
            top: '50',
            left: '40',
            data: ['红头信息', '违规信息', '涉密信息'],
            textStyle: {
              color: '#fff'
            }
          },
          series: [
            {
              name: '访问来源',
              type: 'pie',
              radius: '55%',
              center: ['50%', '40%'],
              data: [
                { name: '红头信息', value: 335 },
                { value: 310, name: '违规信息' },
                { value: 234, name: '涉密信息' },

              ],
              emphasis: {
                itemStyle: {
                  shadowBlur: 10,
                  shadowOffsetX: 0,
                  shadowColor: 'rgba(0, 0, 0, 0.5)'
                }
              }
            }
          ]
        }
      };
    },
    // 事件方法执行
    methods: {},
    // 页面初始化方法
    mounted() {
    
    },
    // 监听值变化
    watch: {},
    // 计算
    computed: {},
  };
</script>

<style scoped lang='scss'>
  .content {
    height: 100%;
    // border: 1px solid red;
  }

  .title {
    color: white;
    font-size: 1.7rem;
    display: flex;
    height: 20%;
    // border: 1px solid red;
  }
</style>