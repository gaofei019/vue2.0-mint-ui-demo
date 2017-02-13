<template>
  <div id="app">
    <mt-header fixed title="fixed top"></mt-header>

    <!--按钮-->
    <div class="btn-box">
        <mt-button type="default">default</mt-button>
        <mt-button type="primary">primary</mt-button>
        <mt-button type="danger">danger</mt-button>
    </div>

    <!-- swipe-->
    <div class="page-swipe">
      <mt-swipe :auto="4000">
        <mt-swipe-item class="slide1">1</mt-swipe-item>
        <mt-swipe-item class="slide2">2</mt-swipe-item>
        <mt-swipe-item class="slide3">3</mt-swipe-item>
      </mt-swipe>
    </div>

    <!--radio-->
    <mt-radio
      title="radio list"
      v-model="value"
      :options="['optionA', 'optionB', 'optionC']">
    </mt-radio>
    <!-- tabbar -->
    <mt-tabbar v-model="selected">
      <mt-tab-item id="tab1">
        <img slot="icon" src="./assets/logo.png">
        tab1
      </mt-tab-item>
      <mt-tab-item id="tab2">
        <img slot="icon" src="./assets/logo.png">
        tab2
      </mt-tab-item>
      <mt-tab-item id="tab3">
        <img slot="icon" src="./assets/logo.png">
        tab3
      </mt-tab-item>
      <mt-tab-item id="tab4">
        <img slot="icon" src="./assets/logo.png">
        tab4
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      selected:'tab1',
      value:'optionA'
    }
  }
}
</script>

<style>
  .btn-box{
    margin-top:50px;
  }
  /* swipe */
  .page-swipe .mint-swipe {
      height: 200px;
      color: #fff;
      font-size: 30px;
      text-align: center;
      margin-bottom: 20px;
  }
  .page-swipe .mint-swipe-item {
      line-height: 200px;
  }
  .page-swipe .slide1 {
      background-color: #0089dc;
      color: #fff;
  }
  .page-swipe .slide2 {
      background-color: #ffd705;
      color: #000;
  }
  .page-swipe .slide3 {
      background-color: #ff2d4b;
      color: #fff;
  }
  .page-swipe-desc {
      text-align: center;
      color: #666;
      margin-bottom: 5px;
  }
</style>
