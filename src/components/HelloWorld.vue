<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-router" target="_blank" rel="noopener">router</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-vuex" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
    <div class="aaa" v-for="(item,index) in list" :key="index">
      <div class="bbb"></div>
      <div class="ccc">
        <div class="ccc_sss" :style="item.svip != ''?'':'padding-top:20px;'" v-if="item.vip">{{item.vip}}</div>
        <div class="ccc_vvv" :style="item.vip != ''?'':'padding-top:20px;'" v-if="item.svip">{{item.svip}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      list:[
        {vip:"vip1",svip:"svip1"},
        {vip:"vip2",svip:"svip2"},
        {vip:"vip3",svip:""},
        {vip:"",svip:"svip4"},
        {vip:"vip5",svip:"svip5"},
        {vip:"vip6",svip:"svip6"}
      ]
    }
  }
}
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
.aaa{
  width: 120px;
  height: 200px;
  background-color: #ccc;
  display: inline-block;
  margin-right: 10px;
  overflow: hidden;
  .bbb{
    width: 100%;
    height: 80px;
    background: #000;
  }
  .ccc{
    width: 100%;
    height: 40px;
    background-color: pink;
    margin-top: 20px;
  .ccc_sss{
    width: 100%;
    height: 20px;
    background:blue;
    color: #fff;
  }
  .ccc_vvv{
    width: 100%;
    height: 20px;
    background:yellow;
    // color: #fff;
  }
  }
}
</style>
