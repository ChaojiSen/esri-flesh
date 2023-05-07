<template>
  <div class="home">
    <!-- 头部导航栏 -->
    <div class="nav"></div>
    <div class="container">
      <!-- 左侧列表 -->
      <div class="left">
        <div class="left-panel panel">
          <div class="left-panel-title"></div>
          <div class="left-panel-container">
            <div class="left">图片</div>
            <div class="right">文字标题</div>
          </div>
        </div>
        <div class="left-panel panel"></div>
        <div class="left-panel panel"></div>
        <div class="left-panel panel"></div>
      </div>
      <!-- 中间展示 -->
      <div class="middle">
        <!-- 地图 -->
        <HomeMap class="map"></HomeMap>
      </div>
      <!-- 右侧列表 -->
      <div class="right"></div>
    </div>
    <div class="bottom">

    </div>

  </div>
</template>

<script>
import * as echarts from 'echarts';

import HomeMap from "./map/HomeMap.vue";

export default {
  components: {
    HomeMap,
  },
};
</script>

<style lang="less" scoped>
.container1 {
  width: 500px;
  height: 200px;
}
.home {
  display: none;
  background: linear-gradient(180deg, rgba(12, 19, 71, 1) 0%, rgba(11, 28, 157, 1) 6.09%, rgba(2, 12, 73, 1) 39.29%, rgba(2, 12, 73, 1) 80.1%, rgba(9, 26, 146, 1) 100%);
  width: 100vw;
  height: 100vh;
}

.nav {
  left: 0px;
  top: 0px;
  width: 100vw;
  height: 86px;
  opacity: 1;
  background: url('../../assets/images/nav.png') no-repeat;
  border: 1px solid rgba(0, 0, 0, 1);
  box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.25);
  margin-bottom: 1px;
  background-size: 100% 100%;
}

.container {
  height: 100%;
  display: flex;
  justify-content: space-between;
  .left {
    flex: 2;
    width: 100%;
    height: 100%;
    background: rgba(255, 255, 255, 1);
    display: flex;
    flex-direction: column;
    .panel{
      height: 100px;
      width: 100%;
    }
    .left-panel-title{
      
    }
  }

  .middle {
    overflow: hidden;
    flex: 3;
    height: 100%;
    width: 100%;
    .map:after {
      content:'';
      display: block;
      visibility: hidden;
    }
  }

  .right {
    flex: 2;
    width: 100%;
    height: 100%;
    background: rgba(255, 255, 255, 1);
    border: 1px solid rgba(0, 0, 0, 1);
    box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.25);
  }

}
.bottom{
    height: 100px;
    width: 100vw;
  }
</style>
