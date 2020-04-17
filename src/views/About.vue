<template>
  <div class="about">
    <h1 class="headline">技术资料</h1>
    <div class="text-p">
      <div style="width:50%;">
        <p class="title_p" @click="program">小程序：</p>
        <div v-if="status">
          <p>1.分佣宝（2018年4月）</p>
          <p>2.选址易【独立】（2019年7月）技术点：{</p>
          <p>uni-app重构（由于IM聊天不可用放弃）</p>
          <p>网易云信IM聊天功能</p>
          <p>vant-weapp（ui组件）</p>
          <p>canvas画布</p>
          <p>腾讯定位</p>
          <p>crypto.js进行数据加密</p>
          <p>}</p>
          <p>难点：</p>
          <p>1.做IM时遇到的语言播放（放在自定义函数中声明会生成多个语音事件，应该放在onload中）</p>
          <p>2.canvas生成图片（图片圆角，多行省略。图片裁剪）</p>
          <p>3.线上版本接收参数（要转码）</p>
          <p>4.for列表图片error展示默认图（绑定error事件，将e，this传过去，将出错图片重新赋值）</p>
          <p>5.cube-ui的横向滚动失效（单独修改样式）</p>
          <p>6.小程序 onLaunch与onload异步请求（promise）</p>
          <p>7.两个scroll-view点击穿透问题（加蒙层，catchtouchmove="preventD"）</p>
        </div>
        <p class="title_p" @click="program2">react项目：</p>
        <div v-if="status2">
          <p>1.PMIS管理后台(旧)（2018年7月）技术点：{</p>
          <p>ant-design</p>
          <p>react</p>
          <p>egg</p>
          <p>}</p>
          <p>2.选址易管理后台【独立】（2018年11月）技术点：{</p>
          <p>ant-design-pro</p>
          <p>egg</p>
          <p>react</p>
          <p>bizcharts（图表）</p>
          <p>高德地图行政区域组件</p>
          <p>crypto.js进行数据加密</p>
          <p>}</p>
          <p>3.PMIS管理后台(新)（2018年7月）技术点：{</p>
          <p>ant-design-pro</p>
          <p>react</p>
          <p>typescript</p>
          <p>egg</p>
          <p>lodash</p>
          <p>}</p>
          <p>难点：</p>
          <p>1.行政区域的使用（渐变颜色）</p>
          <p>2.bizcharts问题（X轴文字太多重叠，旋转角度解决。自定义的纵坐标）</p>
          <p>3.ant-design走马灯组件问题（点击图片显示对应下标的图片，内部还有很多API没有写出来）</p>
        </div>
        <p class="title_p" @click="program6">编程软件：</p>
        <div v-if="status6">
          <p>VScode，HB（uni-app），微信开发者工具，PS6，Charles（抓包），Postman，sublime，studio（flutter），VMware（虚拟机操作linux）</p>
          <p>Xshell，Xftp</p>
          <p>CSDN：https://me.csdn.net/caoyan0829</p>
          <p>牛客：https://www.nowcoder.com/4270576</p>
        </div>
      </div>
      <div style="width:50%;">
        <p class="title_p" @click="program3">vue项目：</p>
        <div v-if="status3">
          <p>1.H5页【独立】 技术点：{</p>
          <p>cube-ui组件</p>
          <p>与app进行通信（HB,Buddy）</p>
          <p>vue-amap</p>
          <p>Clipboard.js（复制）</p>
          <p>lottie（做动画）</p>
          <p>flexible.js（适配）</p>
          <p>}</p>
          <p>2.选址易小程序重构【独立】 技术点：{</p>
          <p>uni-app</p>
          <p>}</p>
          <p>难点：</p>
          <p>1.lottie生成动画</p>
          <p>2.vue中调用小程序的字段</p>
          <p>3.IOS12键盘遮挡页面问题</p>
          <p>4.H5点击复制功能兼容问题（引入插件）</p>
          <p>5.VUE 移动端 input 只能输入数字兼容问题（pattern="[0-9]*" 为了兼容ios）</p>
          <p>6.图片裁剪问题（富文本 图片error时，background-size: cover就没用了，需要使用 object-fit:cover ）</p>
        </div>
        <p class="title_p" @click="program4">HTML项目：</p>
        <div v-if="status4">
          <p>1.H5活动页【独立】 技术点：{</p>
          <p>jq，插件awardrotate.js</p>
          <p>}</p>
          <p>2.企业网站 技术点：{ba</p>
          <p>html+js+css</p>
          <p>}</p>
          <p>难点：</p>
          <p>a标签嵌套a标签位置错乱（给里层的a标签中套上object 标签 ）</p>
        </div>
        <p class="title_p" @click="program5">其它技术：</p>
        <div v-if="status5">
          <p>UI库：</p>
          <p>Bootstrap，cube-ui，ElementUI，vant UI，Ant-design</p>
          <p>其它：</p>
          <p>友盟统计，草料二维码，百度短链接，tinyPNG（图片处理），OSS图片服务，jekins，禅道，TAPD，</p>
          <p>nvm，puppeteer（自测），gitLab，git，nginx（腾讯云配置)</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      status: false,
      status2: false,
      status3: false,
      status4: false,
      status5: false,
      status6: false
    };
  },
  mounted() {},
  methods: {
    program() {
      this.status = !this.status;
    },
    program2() {
      this.status2 = !this.status2;
    },
    program3() {
      this.status3 = !this.status3;
    },
    program4() {
      this.status4 = !this.status4;
    },
    program5() {
      this.status5 = !this.status5;
    },
    program6() {
      this.status6 = !this.status6;
    }
  }
};
</script>
<style lang="less" scoped>
.text-p {
  text-align: left;
  display: flex;
}
.headline{
  text-shadow: 1px 0px 1px purple;
  font-size: 26px;
  margin-bottom: 20px;
}
.title_p{
  cursor: pointer;
  text-shadow: 1px 0px 1px rgb(138, 121, 98);
}
</style>
