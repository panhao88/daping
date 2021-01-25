<template>
  <dv-border-box-8>
    <div class="box">
      <div class="title">
        <div style="margin: 0.5rem 0 0 0.6rem">告警网站排名</div>
      </div>
      <div class="content">
        <div class="swperTitle">
          <div>排名</div>
          <div>内容</div>
          <div>日期</div>
        </div>
        <div class="swiperbox">
          <div class="swiper" ref="swiper">
            <div v-for="(item,index) in arr" :key="index" class="swperItem">
              <div>{{index}}</div>
              <div class="swiperContent">
                <div>123213123122222222222313</div>
              </div>
              <div class="swiperContent">
                <div>dsdsdsdsdsdsdsd222222222222222sdsdsdsdsds</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </dv-border-box-8>
</template>

<script>
  export default {
    name: '',
    // 接收父组件传递过来的参数
    props: {},
    // 注册组件
    components: {},
    // 定义变量
    data() {
      return {
        arr: [
          { content: '11111111111111111111111111111111111111', date: '2011' },
          { content: '22222222222222222222222222222222222222', date: '3011' },
          { content: '33333333333333333333333333333333333333', date: '4011' },
          { content: '44444444444444444444444444444444444444', date: '5011' },
          { content: '55555555555555555555555555555555555555', date: '6011' },
          { content: '66666666666666666666666666666666666666', date: '7011' },
          { content: '77777777777777777777777777777777777777', date: '8011' },
          { content: '888888888888888888888888888888888888888', date: '9011' },
          { content: '1212121212121212121212121212121212121212', date: '10011' },
          { content: '1111134343434343234234234234434111111111', date: '2011' },
          { content: '8888888888888888888888888888888888888888', date: '1551' },
          { content: '68686868686868686868686868686868686866868', date: '100551' },
          { content: '85858555555555555555555555555555555555555', date: '7878' },

        ]
      }
    },
    // 事件方法执行
    methods: {},
    // 页面初始化方法
    mounted() {
    //   const swiper = this.$refs.swiper
    //   let num = -10
    // var time=  setInterval(() => {
    //     swiper.style.top = `${num}%`
    //     num -= 10
    //     if(num==-50){
    //       num=0
    //     }
    //   }, 1000);
    },
    // 监听值变化
    watch: {},
    // 计算
    computed: {}
  }
</script>

<style scoped lang='scss'>
  .box {
    height: 100%;
    width: 100%;
  }



  .title {
    color: white;
    font-size: 1.7rem;
    display: flex;
    height: 10%;
    /* border: 1px solid red; */
  }

  .content {
    height: 90%;
    width: 100%;
    /* border: 1px solid fuchsia; */
  }

  .swperTitle {
    width: 99%;
    height: 7%;
    margin: auto;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-color: white;
    opacity: 0.5;
    /* border: 1px solid firebrick; */
  }


  .swperTitle div:nth-child(1) {
    width: 10%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: rgb(23, 144, 243);
    font-size: 1.4rem;
  }

  .swperTitle div:nth-child(2),
  .swperTitle div:nth-child(3) {
    width: 40%;
    height: 100%;
    /* border: 1px solid red; */
    display: flex;
    justify-content: center;
    align-items: center;
    color: rgb(23, 144, 243);
    font-size: 1.4rem;
  }

  .swiperbox {
    height: 80%;
    width: 100%;
    margin-top: 1rem;
    /* border: 1px solid red; */
    position: relative;
    overflow: hidden;
  }

  .swiper {
    height: 100%;
    width: 100%;
    position: absolute;
    /* border: 1px solid green;  */
    animation: mymove 10s infinite linear;
    /* -webkit-animation: mymove 10s infinite linear;
    /* Safari 和 Chrome */
  }

  
  @keyframes mymove {
    from {
      top: 0px;
    }

    to {
      top: -30%;
    }
  }

  .swperItem {
    display: flex;
    /* border: 1px solid red; */
    width: 100%;
    height: 10%;
    align-items: center;
    color: rgba(11, 160, 247, 0.479);
  }

  .swperItem>div:nth-child(1) {
    width: 10%;
    height: 100%;
    display: flex;
    justify-content: center;
  }

  .swiperContent {
    width: 45%;
    height: 100%;

    display: flex;
    justify-content: center;
    align-items: center;

  }

  .swiperContent>div {
    width: 70%;
    height: 100%;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    /* border: 1px solid red; */
    vertical-align: middle;
  }
</style>