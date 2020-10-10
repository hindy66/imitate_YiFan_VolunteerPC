<template>
  <div class="bottom-bar-box">
    <el-row>
      <el-col :span="8">
        <div class="left-title">
          益帆公益服务平台
        </div>
      </el-col>
      <el-col :span="16">
        <div class="right-info">
          <span>©2019 益帆公益服务平台  丨</span>
          <span>粤ICP备17157276号</span>
          <span>丨  佛山市益帆网络有限公司 版权所有</span>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name:'BottomBar'
}
</script>

<style scoped>
  @media screen and (max-width:1200px){
    .bottom-bar-box{
      width: 1200px;
      margin: 0 auto;
    }
  }
  @media screen and (min-width:1200px) and (max-width:1400px){
    .bottom-bar-box{
      width: 1200px;
      margin: 0 auto;
    }
  }
  @media screen and (min-width:1400px){
    .bottom-bar-box{
      width: 1400px;
      margin: 0 auto;
    }
  }
  .bottom-bar-box{
    height: 60px;
    line-height: 60px;
    position: relative;
    box-sizing: border-box;
    background-image:url('/images/bottom_background.png');
  }
  .bottom-bar-box .left-title{
    font-size: 20px;
    color: white;
    margin-left: 20px;
  }
  .bottom-bar-box .right-info{
    /* display: flex;
    justify-content: flex-end; */
    margin-right: 20px;
    text-align: right;
    color: #999;
  }

</style>
