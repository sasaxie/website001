<template>
  <div id="app">
    <el-row>
      <el-col :span="12">
        <div style="float: right;">
          <h1 style="color: #4b5cc4;  margin-right: 200px;">宇宙暴力极光采集加工有限公司</h1>
          <span style="color: #c2ccd0;">主营产品：极光加工</span>
        </div>
      </el-col>
      <el-col :span="12">
        <el-menu :default-active="defaultIndex" mode="horizontal">
          <el-menu-item index="1">首页</el-menu-item>
          <el-menu-item index="2">公司简介</el-menu-item>
          <el-menu-item index="3">产品展示</el-menu-item>
          <el-menu-item index="4">新闻资讯</el-menu-item>
          <el-menu-item index="5">留言中心</el-menu-item>
          <el-menu-item index="6">联系我们</el-menu-item>
        </el-menu>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <el-carousel :interval="5000" arrow="always" height="400px">
          <el-carousel-item v-for="(image, index) in imageList" :key="index">
            <el-image style="width: 100%; height: 100%" :src="image.path" fit="none"></el-image>
          </el-carousel-item>
        </el-carousel>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <div style="height: 100px;"></div>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <div :style="{backgroundImage: `url(${image2})`}" style="height: 520px; display: flex; align-items: center; justify-content: center;">
          <div style="height: 320px; width: 1115px;">
            <div style="width: 437px; height:100%; background-color: green; float: left;">
              <img src="./assets/3.jpg" style="width: 100%; height: 100%;">
            </div>
            <div style="width: 678px; height:100%; background-color: rgba(0, 0, 0, 0.1); float: right;">
              <br/>
              <br/>
              <span style="color: white; font-size: 24px; font-weight: bold; margin-left: 30px;">关于我们</span><br/>
              <div style="margin-left: 30px; margin-top: 30px; margin-right: 20px;">
                <span style="color: white; font-size: 14px;">公司秉承“顾客至上，锐意进取”的经营理念，坚持“客户第一”的原则为广大客户提供优质的服务。欢迎惠顾</span>
              </div>
              <el-button style="margin-top: 30px; margin-left: 30px;" type="warning">查看更多</el-button>
            </div>
          </div>
        </div>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <div style="height: 100px;"></div>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="24">
        <div style="height: 319px; width: 1920px; display: flex; align-items: center; justify-content: center;">
          <div style="height: 319px; width: 1200px;">
            <h2 style="color: #1e50ae; font-size: 24px; text-align: center;">产品展示</h2>
            <p style="color: #666;width: 62px; margin: 0 auto;">Products</p>
            <a style="margin: 30px auto; width: 202px; height: 55px; display: block; background-color: #1e50ae; border-radius: 20px; line-height: 55px; color: #fff; text-align: center; font-size: 16px;">查看更多</a>
            <div>烟台恒力激光切割加工有限公司坐落在中国-山东-烟台-烟台市内，是集塑胶加工为一体的专业产品服务提供商，具有雄厚的科研实力、技术实力和经济实力。产品以雄厚的技术力量、先进的设备、精湛的工艺在同行业中达到较高水平。烟台恒力激光切割加工有限公司联系电话：86-135-62501640,提供塑胶加工等产品批发、供应，欢迎广大新老客户来电咨询价格、加盟、招商等服务。</div>
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      defaultIndex: "1",
      image2: require("./assets/2.jpg"),
      imageList: [
        { path: require("./assets/1.jpg") },
        { path: require("./assets/1.jpg") },
        { path: require("./assets/1.jpg") },
        { path: require("./assets/1.jpg") }
      ]
    };
  }
};
</script>

<style>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>
