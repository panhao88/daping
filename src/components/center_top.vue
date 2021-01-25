<template>
  <dv-border-box-8 :reverse="true">
    <div class="box">
      <div class="title">
        <div style="margin: 0.5rem 0 0 0.6rem">信息总量</div>
      </div>
      <div class="info">
        <div style="width: 49%">
          <div class="infoCount">
            告警信息总量：<countTo
              :startVal="startVal"
              :endVal="alarmEndVal"
              :duration="3000"
              style="
                font-size: 1.7rem;
                color: rgb(115, 219, 247);
                text-shadow: 0px 0px 15px rgb(144, 231, 255);
              "
            ></countTo>
          </div>
          <div class="infoCount">
            红头信息总量：
            <countTo
              :startVal="startVal"
              :endVal="violationEndVal"
              :duration="3000"
              style="
                font-size: 1.7rem;
                color: rgb(217, 125, 54);
                text-shadow: 0 0 15px rgb(217, 125, 54);
              "
            ></countTo>
          </div>
        </div>
        <div style="width: 49%">
          <div class="infoCount">
            违规信息总量：
            <countTo
              :startVal="startVal"
              :endVal="redEndVal"
              :duration="3000"
              style="
                font-size: 1.7rem;
                color: rgb(55, 199, 41);
                text-shadow: 0 0 15px rgb(55, 199, 41);
              "
            ></countTo>
          </div>
          <div class="infoCount">
            涉密文件总量：<countTo
              :startVal="startVal"
              :endVal="wadeAirtightEndVal"
              :duration="3000"
              style="
                font-size: 1.7rem;
                color: deeppink;
                text-shadow: 0 0 15px deeppink;
              "
            ></countTo>
          </div>
        </div>
      </div>
    </div>
  </dv-border-box-8>
</template>
  
<script>
import countTo from "vue-count-to";
export default {
  name: "",
  // 接收父组件传递过来的参数
  props: {},
  // 注册组件
  components: {
    countTo,
  },
  // 定义变量
  data() {
    return {
      startVal: 0,
      alarmEndVal: 2017, // 告警数据总数
      violationEndVal: 2000, // 违规数据总数
      redEndVal: 1920, // 红头数据
      wadeAirtightEndVal: 2602, //涉密文件总量
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
div {
  color: white;
}

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

.info {
  display: flex;
  width: 100%;
  height: 80%;
}

.infoCount {
  font-size: 1.5rem;
  width: 100%;
  height: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
