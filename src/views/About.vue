<template>
  <div class="about">
    <h1 class="headline">技术资料</h1>
    <div class="text-p">
      <!-- 左 -->
      <div style="width:50%;padding:0px 20px;">
        <div class="title_p" @click="program">
          <p class="title_t">小程序：</p>
          <i v-if="status" class="el-icon-arrow-down arrows"></i>
          <i v-else class="el-icon-arrow-right arrows"></i>
        </div>
        <div v-if="status" class="content_introduce">
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
        <div class="title_p" @click="program2">
          react项目：
          <i v-if="status2" class="el-icon-arrow-down arrows"></i>
          <i v-else class="el-icon-arrow-right arrows"></i>
        </div>
        <div v-if="status2" class="content_introduce">
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
        <div class="title_p" @click="program6">
          编程软件：
          <i v-if="status6" class="el-icon-arrow-down arrows"></i>
          <i v-else class="el-icon-arrow-right arrows"></i>
        </div>
        <div v-if="status6" class="content_introduce">
          <p>VScode，HB（uni-app），微信开发者工具，PS6，Charles（抓包），Postman，sublime，studio（flutter），VMware（虚拟机操作linux）</p>
          <p>Xshell，Xftp</p>
          <p>
            CSDN：
            <a href="https://me.csdn.net" target="view_window">https://me.csdn.net</a>
          </p>
          <p>
            牛客：
            <a href="https://www.nowcoder.com" target="view_window">https://www.nowcoder.com</a>
          </p>
        </div>
        <p class="title_p" @click="program7">
          容易忽视的git命令：
          <i v-if="status7" class="el-icon-arrow-down arrows"></i>
          <i v-else class="el-icon-arrow-right arrows"></i>
        </p>
        <div v-if="status7" class="content_introduce">
          <p>git branch (查看全部分支)</p>
          <p>git checkout -b xxx (创建分支)</p>
          <p>git checkout xxx (切换分支)</p>
          <p>git merge xxx (合并分支)</p>
          <p>git update-index --assume-unchanged /路径 (已经提交到线上储存库中，后期修改不提交文件->忽略文件)</p>
          <p>git update-index --no-assume-unchanged /路径 (已经提交到线上储存库中，后期修改不提交文件->恢复忽略文件)</p>
        </div>
      </div>
      <!-- 右 -->
      <div style="width:50%;padding:0px 20px;">
        <p class="title_p" @click="program3">
          vue项目：
          <i v-if="status3" class="el-icon-arrow-down arrows"></i>
          <i v-else class="el-icon-arrow-right arrows"></i>
        </p>
        <div v-if="status3" class="content_introduce">
          <p>1.H5页【独立】 技术点：{</p>
          <p>vue项目UI框架：Vue-Blu - vue-strap - vuetify - iView - Element</p>
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
        <p class="title_p" @click="program4">
          HTML项目：
          <i v-if="status4" class="el-icon-arrow-down arrows"></i>
          <i v-else class="el-icon-arrow-right arrows"></i>
        </p>
        <div v-if="status4" class="content_introduce">
          <p>1.H5活动页【独立】 技术点：{</p>
          <p>jq，插件awardrotate.js</p>
          <p>}</p>
          <p>2.企业网站 技术点：{ba</p>
          <p>html+js+css</p>
          <p>}</p>
          <p>难点：</p>
          <p>a标签嵌套a标签位置错乱（给里层的a标签中套上object 标签 ）</p>
        </div>
        <p class="title_p" @click="program8">
          CSS：
          <i v-if="status8" class="el-icon-arrow-down arrows"></i>
          <i v-else class="el-icon-arrow-right arrows"></i>
        </p>
        <div v-if="status8" class="content_introduce">
          <p>css选择器优先级： !important ——>行内选择器——>ID选择器——>类选择器——>元素选择器——>通配符选择器——>继承父级样式——>浏览器默认属性</p>
        </div>
        <p class="title_p" @click="program5">
          其它技术：
          <i v-if="status5" class="el-icon-arrow-down arrows"></i>
          <i v-else class="el-icon-arrow-right arrows"></i>
        </p>
        <div v-if="status5" class="content_introduce">
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
      status6: false,
      status7: false,
      status8: false
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
    },
    program7() {
      this.status7 = !this.status7;
    },
    program8() {
      this.status8 = !this.status8;
    },
    program9() {
      this.status9 = !this.status9;
    }
  }
};
</script>
<style lang="less" scoped>
.text-p {
  text-align: left;
  display: flex;
}
.headline {
  text-shadow: 1px 0px 1px purple;
  font-size: 26px;
  margin-bottom: 20px;
}

.title_p {
  cursor: pointer;
  text-shadow: 1px 0px 1px rgb(138, 121, 98);
  position: relative;
  padding: 5px;
  &:hover {
    color: #fffffd;
  }
  &:hover::before {
    border-radius: 10px 20px 10px 20px;
    content: "";
    height: 100%;
    width: 100%;
    opacity: 0.5;
    position: absolute;
    left: 0px;
    top: 0px;
    background: -moz-linear-gradient(
      45deg,
      #c6f0ef 33%,
      #cfcbe2 34%,
      #cfcbe2 59%,
      #c6f0ef 60%
    ); /* FF3.6+ */
    background: -webkit-gradient(
      linear,
      left bottom,
      right top,
      color-stop(33%, #c6f0ef),
      color-stop(34%, #cfcbe2),
      color-stop(59%, #cfcbe2),
      color-stop(60%, #c6f0ef)
    ); /* Chrome,Safari4+ */
    background: -webkit-linear-gradient(
      45deg,
      #c6f0ef 33%,
      #cfcbe2 34%,
      #cfcbe2 59%,
      #c6f0ef 60%
    ); /* Chrome10+,Safari5.1+ */
    background: -o-linear-gradient(
      45deg,
      #c6f0ef 33%,
      #cfcbe2 34%,
      #cfcbe2 59%,
      #c6f0ef 60%
    ); /* Opera 11.10+ */
    background: -ms-linear-gradient(
      45deg,
      #c6f0ef 33%,
      #cfcbe2 34%,
      #cfcbe2 59%,
      #c6f0ef 60%
    ); /* IE10+ */
    background: linear-gradient(
      45deg,
      #c6f0ef 33%,
      #cfcbe2 34%,
      #cfcbe2 59%,
      #c6f0ef 60%
    ); /* W3C */
    filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#c6f0ef', endColorstr='#c6f0ef', GradientType=1); /* IE6-9 fallback on horizontal gradient */
    background-size: 60px 30px;
    color: #fff;
    -webkit-animation: load 0.2s ease-in;
  }
  .arrows {
    position: absolute;
    right: 0px;
    top: 9px;
  }
}
.content_introduce {
  p {
    padding: 4px 20px;
  }
}

@-webkit-keyframes load {
  0% {
    width: 0%;
  }
  100% {
    width: 100%;
  }
}
</style>
