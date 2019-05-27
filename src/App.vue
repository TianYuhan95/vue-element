<template>
  <el-container>
    <el-header>
      <el-row style="background-color: #555555">
        <el-col :span="6">
          <el-col :span="10">
            <div class="logo">
              <a>
                <el-image style="height: 68px;width:68px" :src="url" :fit="scale-down"></el-image>
              </a>
            </div>
          </el-col>
          <el-col :span="14">
            <div class="logo-text">
              <b>AI开放平台</b>
            </div>
          </el-col>
        </el-col>
        <el-col :span="12">
          <el-row style="min-height: 61px"></el-row>
          <el-row>
            <el-menu id="el-menu"
                     :default-active="activeIndex"
                     class="el-menu--horizontal"
                     mode="horizontal"
                     @select="handleSelect"
                     background-color="#555"
                     text-color="#fff"
                     active-text-color="#ffd04b">
              <el-menu-item index="1">首页</el-menu-item>
              <el-submenu index="2">
                <template slot="title">在线试用</template>
                <el-submenu index="2-1">
                  <template slot="title">语音合成</template>
                  <el-menu-item index="2-1-1">在线语音合成</el-menu-item>
                </el-submenu>
                <el-submenu index="2-2">
                  <template slot="title">语音识别</template>
                  <el-menu-item index="2-2-1">语音听写</el-menu-item>
                  <el-menu-item index="2-2-2">语音转写</el-menu-item>
                  <el-menu-item index="2-2-3">短语音转写</el-menu-item>
                </el-submenu>
                <el-submenu index="2-4">
                  <template slot="title">选项4</template>
                  <el-menu-item index="2-4-1">选项1</el-menu-item>
                  <el-menu-item index="2-4-2">选项2</el-menu-item>
                  <el-menu-item index="2-4-3">选项3</el-menu-item>
                </el-submenu>
              </el-submenu>
              <el-menu-item index="3" disabled>消息中心</el-menu-item>
              <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item>
            </el-menu>
          </el-row>
        </el-col>
      </el-row>
    </el-header>
    <el-main></el-main>
    <el-footer></el-footer>
  </el-container>
  <!--<router-view/>-->
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      activeIndex: '1',
      url: require("../static/image/logo.png")
    };
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
