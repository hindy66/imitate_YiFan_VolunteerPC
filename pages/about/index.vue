<template>
  <div class="about-box">
    <!-- 顶部大广告图部分 -->
    <div class="banner-about">
      <div class="banner-about-content">
        <div class="banner-title">
          <p>益帆公益</p>
          <p>做公益，益帆与你同行爱心活动</p>
        </div>
      </div>
    </div>
    <!-- 什么是益帆部分 -->
    <div class="middel-part-box">
      <div class="middel-part">
        <div class="middle-img">
          <img src="/images/what_pic.png">
        </div>
        <div class="middle-content">
          <h3>益帆是什么？</h3>
          <!-- 分割线 -->
          <div class="padding-line"></div>
          <div class="what-intro">
            <span>
              我们是致力于将公益基金机构，公益主办机构和爱心志愿者联系起来的平台。我们愿意接受严格的财务监控和内外审计
              ，我们将严格把手公益基金机构的资金真正落实在公益活动中，让公益活动更快，更简单，更方便并真实地在中国各地精彩地举办起来，
              让更多的爱心志愿者参与进来。
            </span>
          </div>
        </div>
    </div>
    </div>
    <!-- 益帆能帮助你什么部分 -->
    <div class="middle-second-part-box">
      <div class="middle-second-part">
        <div class="second-part-content">
          <h3>益帆能帮助你什么</h3>
          <span>
              帮助基金机构在短时间内找到可靠的合作伙伴举办公益活动，跟进项目进度；
              帮助活动机构最大限度降低人力劳动成本，时间成本和维护机构间的相互利益；
              帮助爱心志愿者更容易寻找公益活动的机会。
            </span>
        </div>
        <div class="second-part-img">
          <img src="/images/help_pic01.png">
        </div>
      </div>
    </div>
    <!-- 底部平台使用角色介绍部分 -->
    <div class="middle-bottom-part-box">
      <div class="middle-bottom-part">
        <div class="role-item">
          <img src="/images/help_pic02.png">
          <span class="role-name">公益基金协会</span>
          <span class="role-detail">一个可以寻找有资质，有质量的活动机构和跟进中标活动进度的信息平台。</span>
        </div>
        <div class="role-item">
          <img src="/images/help_pic03.png">
          <span class="role-name">活动机构</span>
          <span class="role-detail">一个可以投标基金项目，发布活动信息，招揽志愿者的公益信息集中平台。</span>
        </div>
        <div class="role-item">
          <img src="/images/help_pic04.png">
          <span class="role-name">爱心志愿者</span>
          <span class="role-detail">一个可以让爱心志愿者收集资料及参与公益活动的平台。</span>
        </div>
      </div>
    </div>
    <div class="fixed-code">
      <img  class="arrow-top" src="/images/scroll_top.png">
      <img src="/images/app_download.png" @click="showCode">
    </div>
    <!-- app下载二维码对话框 -->
    <el-dialog
      title="App下载"
      :visible.sync="dialogVisible"
      width="40%"
      center>
      <img src="images/app_download_code.png">
    </el-dialog>
  </div>
</template>

<script>
export default {
  name:'About',
  data() {
    return {
      //  app下载对话框的显示和隐藏
      dialogVisible:false
    }
  },
  mounted() {
    //  监听当前窗口的滚动事件
    window.addEventListener('scroll', this.arrowShow)
  },
  methods: {
    arrowShow(){
      let scrollTop = document.documentElement.scrollTop || document.body.scrollTop
      let arrowObj = document.querySelector('.arrow-top')
      if(scrollTop > 100){
        arrowObj.style.display = 'block'
      }
      else{
        arrowObj.style.display = 'none'
      }
    },
    showCode(){
      this.dialogVisible = true
    }
  },
}
</script>

<style scoped>
@media screen and (max-width: 1200px){
  .about-box{
    width: 1200px;
  }
  .banner-about{
    width: 1200px;
    height:520px;
    background-image: url('/images/banner.jpg');
    background-size:100% 520px;
    background-repeat: no-repeat;
    display: block;
    margin:0 auto;
  }
  .middel-part-box,
  .middle-second-part-box,
  .middle-bottom-part-box{
    width: 1200px;
  }
}

@media screen and (min-width:1200px) and (max-width: 1400px) {
  .about-box{
    width: 1200px;
  }
  .banner-about{
    width: 1200px;
    height:520px;
    background-image: url('/images/banner.jpg');
    background-size:100% 520px;
    background-repeat: no-repeat;
    display: block;
    margin: 0 auto;
  }
  .middel-part-box,
  .middle-second-part-box,
  .middle-bottom-part-box{
    width: 1200px;
  }
}
@media screen and (min-width: 1400px){
  .banner-about{
    width: 1400px;
    height:520px;
    background-image: url('/images/banner.jpg');
    background-size:100% 520px;
    background-repeat: no-repeat;
    display: block;
    margin:0 auto;
  }
  .middel-part-box,
  .middle-second-part-box,
  .middle-bottom-part-box{
    width: 1400px;
  }
}
.about-box{
  margin: 0 auto;
}
.banner-about-content{
    display: inline-block;
  }
  .banner-title{
    text-align: left;
    font-weight: bold;
    font-size: 60px;
    line-height: 86px;
    color: #333333;
    margin:  60px  0 0 100px;
  }
  .banner-title p{
    margin: 0 auto;
  }
  .middel-part-box,
  .middle-second-part-box,
  .middle-bottom-part-box{
    background-image: linear-gradient(to right, #F9F5F6, #FCFAFB, #FFFFFF);
    margin: 0 auto;
  }
  .middel-part,
  .middle-second-part,
  .middle-bottom-part{
    width: 1200px;
    padding: 80px 0;
    /* height: 500px; */
    display: flex;
    justify-content:space-around;
    position: relative;
    margin: 0 auto;
  }
  .middle-img{
    margin-right: 60px;
  }
  .middle-content h3,
  .middle-second-part h3{
    font-size: 48px;
    text-align: left;
  }
  .middle-content h3::after,
  .middle-second-part h3::after{
    content: '';
    display: block;
    width: 80px;
    height: 5px;
    background-color: #ff6969;
    /* margin-bottom: 60px; */
  }
  .what-intro span,
  .middle-second-part span{
    line-height: 38px;
    display: block;
    width: 700px;
    font-size: 15px;
    text-align: left;
  }

  .middle-second-part-box{
    display: flex;
    justify-content: center;
    background-image: linear-gradient(to right, #FFFFFF, #FCFAFB, #F9F5F6);
    padding: 80px 0;
  }

  .middle-bottom-part-box{
    background-color: white;
  }
  .middle-bottom-part span{
    display: block;
    width: 300px;
    text-align: center;
  }
  .middle-bottom-part .role-name{
    width: 300px;
    height: 60px;
    margin-top: -20px;
    border-radius: 30px;
    text-align: center;
    color: white;
    font-size: 26px;
    line-height: 60px;
    position: relative;
    z-index: 6;
  }
  .middle-bottom-part .role-item:first-child .role-name{
    background-color: #9B9EFF;
  }
  .middle-bottom-part .role-item:nth-child(2) .role-name{
    background-color: #FF92AA;
  }
  .middle-bottom-part .role-item:nth-child(3) .role-name{
    background-color: #F9C576;
  }
  .fixed-code{
    position: fixed;
    z-index: 999;
    top: 81px;
    right: 100px;
  }
  .fixed-code img{
    display:block;
    cursor: pointer;
  }
  .fixed-code img:first-child{
    margin-bottom: 10px;
    display: none;
  }
</style>
