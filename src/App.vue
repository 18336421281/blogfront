<template>
  <div id="app">
    <router-view :IsPC="IsPC" />
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      IsPC: this.getIsPC()
    };
  },
  methods: {
    getIsPC() {
      if(window.screen.width > 960){
        return true;
      }
      return false;
    }
  }
};
</script>

<style>
.pc20 {
  padding: 0px 20% !important;
}

* {
  margin: 0;
  padding: 0;
  border: 0;
}
#app {
  height: 100%;
}
* {
  font-family: "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB",
    "Microsoft YaHei", "微软雅黑", Arial, sans-serif;
}
a {
  text-decoration: none;
}
.router-link-active {
  text-decoration: none;
}
.shuxian {
  background-color: rgb(139, 139, 139);
  height: 50px;
  width: 1px;
}
.hengxian {
  background-color: rgb(218, 218, 218);
  height: 1px;
  width: 100%;
}
.selectItem {
  box-shadow: 0px 1px 8px 0px rgb(168, 168, 168) !important;
  background-color: #303133 !important;
}
</style>
