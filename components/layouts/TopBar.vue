<template>
    <div class="top-bar-box">
      <div class="top-bar-container">
        <!-- 左侧内容 -->
        <div class="head-left">
          <div class="top-bar-title">
            <a>益帆公益服务平台</a>
          </div>
          <!-- 分割线 -->
          <div class="padding-line">
            |
          </div>
          <!-- 页面切换栏 -->
          <div class="left-content">
              <li v-for="item in leftContentList" @click="topNavItemClick(item)"><a :class="{'active':isSelected == item.path}">{{item.title}}</a></li>
          </div>
        </div>
        <!-- 右侧内容 -->
        <div class="head-right">
          <!-- 消息小图标 -->
          <div class="right-item">
            <el-badge :value="msgCount" class="el-icon-chat-line-round" :hidden="msgCount == 0"></el-badge>
          </div>
          <div class="register"><span>注册</span></div>
          <div class="login"><span>登录</span></div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'TopBar',
  data() {
    return {
      isSelected:'/about',
      leftContentList:[
        {title:'首页', path:'/home'},
        {title:'项目大厅',path:'/lobby'},
        {title:'关于益帆',path:'/about'},
      ],
      msgCount:0
    }
  },
  methods: {
    topNavItemClick(item){
      this.isSelected = item.path
      this.$router.push(item.path)
    }
  },
}
</script>

<style scoped>
  @media screen and (max-width:1200px){
    .top-bar-box{
      width: 1200px;
      height: 81px;
      background: white;
      line-height: 81px;
      position: relative;
      box-sizing: border-box;
      margin: 0 auto;
    }
  }
  @media screen and (min-width:1200px) and (max-width:1400px){
    .top-bar-box{
      width: 1200px;
      height: 81px;
      background: white;
      line-height: 81px;
      position: relative;
      box-sizing: border-box;
      margin: 0 auto;
    }
  }
  @media screen and (min-width:1400px){
    .top-bar-box{
      width: 1400px;
      height: 81px;
      background: white;
      line-height: 81px;
      position: relative;
      box-sizing: border-box;
      margin: 0 auto;
    }
  }
  .top-bar-container{
      padding: 0 20px;
      box-sizing: border-box;
      margin:0 auto;
    }
    .top-bar-title{
      font-size: 20px;
      font-weight: bold;
      cursor: pointer;
      float: left;
    }
    .head-left{
      width: 50%;
      min-width: 600px;
      height: 81px;
      display: inline-block;
    }
    .padding-line{
      width: 4px;
      height: 81px;
      color: gray;
      float: left;
      font-size: 30px;
      margin: 0 0 0 40px;
    }
    .left-content{
      width: 800px;
    }
    .left-content  li{
      display: inline-block;
      width: 140px;
      font-size: 16px;
      text-align: center;
    }
    .left-content a{
      padding: 5px 0;
    }
    .left-content a:hover{
      color:#FF6969 ;
    }
    .left-content  a.active{
      font-weight: bold;
      color: #FF6969;
      border-bottom: 2px solid #FF6969;
    }
    .head-right{
      float: right;
      min-width: 200px;
      display: flex;
      justify-content: space-around;
      align-items: center;
    }
    .head-right .right-item,
    .head-right div span{
      cursor: pointer;
    }
    .head-right .right-item:hover,
    .head-right div span:hover{
      color: #FF6969;
    }
</style>
