<template>
  <dv-full-screen-container class="box">
    <!-- 整体边框 -->
    <dv-border-box-1>
      <!-- padding后的盒子 -->
      <div class="content">
        <!-- 标题 -->
        <div class="title">
        <dv-decoration-7 >来了大佬</dv-decoration-7>
        </div>
        <!-- 顶部 -->
        <div class="boxTop">
          <!-- 上左-->
          <div class="inner">
            <leftTop></leftTop>
          </div>
          <!-- 上中 -->
          <div class="inner">
            <centerTop></centerTop>
          </div>
          <!-- 上右 -->
          <div class="inner">
            <rightTop></rightTop>
          </div>
        </div>
        <!-- 底部 -->
        <div class="boxBottom">
          <!-- 下左 -->
          <div class="inner">
            <leftBottom></leftBottom>
          </div>
          <!-- 下中 -->
          <div class="inner">
            <centerBottom></centerBottom>
          </div>
          <!-- 下右 -->
          <div class="inner">
            <rightBottm></rightBottm>
          </div>
        </div>
      </div>
    </dv-border-box-1>
  </dv-full-screen-container>
</template>

<script>
import leftTop from "../components/left_top";
import centerTop from "../components/center_top";
import rightTop from "../components/right_top";
import leftBottom from "../components/left_bottom";
import centerBottom from "../components/center_bottom.vue";
import rightBottm from "../components/right_bottom";
export default {
  name: "",
  // 接收父组件传递过来的参数
  props: {},
  // 注册组件
  components: {
    leftTop,
    centerTop,
    rightTop,
    leftBottom,
    centerBottom,
    rightBottm,
  },
  // 定义变量
  data() {
    return {
      flag: true,
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
/*最外层盒子  保证占满全屏 */
.box {
  width: 100vh;
  height: 100vw;
  background: rgb(24, 26, 29);
}
// 边框内的盒子  作用:存放所有的内容
.content {
  width: 100%;
  height: 100%;
}

// 顶部标题
.title {
  height: 8%;
  font-size: 3rem;
  color: white;
  // border:1px solid red;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* 控制盒子边框 */
.inner {

  width: 33%;
  height: 100%;
}

.boxTop {
  width: 98%;
  height: 25%;
  margin: 0 auto;
  display: flex;
  justify-content: space-around;

}

.boxBottom {
  width: 98%;
  height: 63%;
  margin: 0 auto;
  margin-top: 0.4rem;
  margin-bottom: 10px;
  display: flex;
  // border: 1px solid green;
}
</style>