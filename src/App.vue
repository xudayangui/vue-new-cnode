<template>
  <div id="app">
    <Header />
    <div class='main-section'>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
/**
 * 项目的入口Vue文件，
 * 在这里进行‘整体布局’，比如上面最简单的布局方式：
 * 上一块 - 下一块
 */
import Header from "@/components/Header.vue";

export default {
  /**
   * 给此组件起的名字，会显示在Vue的DevTool里面
   */
  name: "app",
  /**
   * 注册引用进来的其他组件
   */
  components: {
    Header
  }
};
</script>

<style>
#app {
  font-family: "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB",
    "Microsoft YaHei", "微软雅黑", Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: rgba(0, 0, 0, 0.65);
  font-size: 14px;
}

* {
  /* overflow: hidden; */
  margin: 0;
  padding: 0;
}
*::-webkit-scrollbar {
	/*滚动条整体样式*/
	width: 4px;/*定义纵向滚动条宽度*/
	height: 8px;/*定义横向滚动条高度*/
}

*::-webkit-scrollbar-thumb {
	/*滚动条内部滑块*/
	border-radius: 8px;
	background-color: hsla(240, 1%, 17%, 0.603);
	transition: background-color 0.3s;
}

*::-webkit-scrollbar-thumb:hover {
	/*鼠标悬停滚动条内部滑块*/
	background: #bbb;
}

*::-webkit-scrollbar-track {
	/*滚动条内部轨道*/
	background: #ededed;
}
</style>

<style lang="scss" scoped>
.main-section {
  margin: auto;
  width: 1200px;
}
</style>

