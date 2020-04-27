<template>
  <div class="hello">
    <div class="aaa" v-for="(item,index) in list" :key="index">
      <div class="bbb"></div>
      <div class="ccc">
        <div
          class="ccc_sss"
          :style="item.svip?'':'padding-top:20px;'"
          v-if="item.vip"
        >{{item.vip}}</div>
        <div
          class="ccc_vvv"
          :style="item.vip?'':'padding-top:20px;'"
          v-if="item.svip"
        >{{item.svip}}</div>
      </div>
    </div>
    <!-- 进度条 -->
    <div id="progress">
      <span></span>
    </div>
    <div class="goToUrl" @click="$router.push('/Page-practice')">练习页面</div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
    something:''
  },
  data() {
    return {
      list: [
        { vip: "vip1", svip: "svip1" },
        { vip: "vip2", svip: "svip2" },
        { vip: "vip3", svip: "" },
        { vip: "", svip: "svip4" },
        { vip: "vip5", svip: "svip5" },
        { vip: "vip6", svip: "svip6" }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.hello{
  width: 300px;
  margin: 0 auto;
}
.aaa {
  width: 120px;
  height: 200px;
  background-color: #ccc;
  display: inline-block;
  margin-right: 10px;
  overflow: hidden;
  margin-bottom: 10px;
  .bbb {
    width: 100%;
    height: 80px;
    background: #000;
  }
  .ccc {
    width: 100%;
    height: 40px;
    background-color: pink;
    margin-top: 20px;
    .ccc_sss {
      width: 100%;
      height: 20px;
      background: blue;
      color: #fff;
    }
    .ccc_vvv {
      width: 100%;
      height: 20px;
      background: yellow;
      // color: #fff;
    }
  }
}
#progress {
  width: 50%;
  height: 20px;
  border: 1px solid #ccc;
  border-radius: 15px;
  margin: 0 auto;
  overflow: hidden;
  box-shadow: 0 0 5px 0px #ddd inset;
}

#progress span {
  display: inline-block;
  width: 100%;
  height: 100%;
  background: #2989d8; /* Old browsers */
  /* linear-gradient() 函数用于创建一个线性渐变的 "图像",也就是渐变背景 */
  background: -moz-linear-gradient(
    45deg,
    #2989d8 33%,
    #7db9e8 34%,
    #7db9e8 59%,
    #2989d8 60%
  ); /* FF3.6+ */
  background: -webkit-gradient(
    linear,
    left bottom,
    right top,
    color-stop(33%, #2989d8),
    color-stop(34%, #7db9e8),
    color-stop(59%, #7db9e8),
    color-stop(60%, #2989d8)
  ); /* Chrome,Safari4+ */
  background: -webkit-linear-gradient(
    45deg,
    #2989d8 33%,
    #7db9e8 34%,
    #7db9e8 59%,
    #2989d8 60%
  ); /* Chrome10+,Safari5.1+ */
  background: -o-linear-gradient(
    45deg,
    #2989d8 33%,
    #7db9e8 34%,
    #7db9e8 59%,
    #2989d8 60%
  ); /* Opera 11.10+ */
  background: -ms-linear-gradient(
    45deg,
    #2989d8 33%,
    #7db9e8 34%,
    #7db9e8 59%,
    #2989d8 60%
  ); /* IE10+ */
  background: linear-gradient(
    45deg,
    #2989d8 33%,
    #7db9e8 34%,
    #7db9e8 59%,
    #2989d8 60%
  ); /* W3C */
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#2989d8', endColorstr='#2989d8', GradientType=1); /* IE6-9 fallback on horizontal gradient */
  background-size: 60px 30px;
  color: #fff;
  -webkit-animation: load 3s  ease-in;
}

@-webkit-keyframes load {
  0% {
    width: 0%;
  }
  100% {
    width: 100%;
  }
}
.goToUrl{
  cursor: pointer;
}
</style>
