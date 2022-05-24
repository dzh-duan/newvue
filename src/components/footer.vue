
<template>
  <div id="boby">
    <router-link class="home"  to="/home"><span class="iconfont icon-zhuye"></span> </router-link>
    <router-link class="activity"  to="/activity"><span class="iconfont icon-goutongye_santiaogang_tiaozhuanxuanzehaizi"></span></router-link>
    <router-link class="pay"  to="/pay"><span class="iconfont icon-zuoyouhuadong"></span></router-link>
    <router-link class="service"  to="/service"><span class="iconfont icon-kefu"></span></router-link>
    <router-link class="user" to="/user"><span class="iconfont icon-gerenzhongxin"></span></router-link>
  </div>
</template>
<style lang="scss" scoped>
    #boby {
        width:100%;
        display: flex;
        justify-content:center;
        padding-right: 1px;
        z-index: 999;
        background: rgba(255, 255, 255, 0.90);
        box-shadow: 0px -3px 10px rgb(0 0 0 / 10%);
      .router-link-active{
        color: #6d00be;
      }
        a{
            color: #bbbbbb;
            width: 20%;
            height: 60px;
            span {
              font-size: 24px;
              display:inline-block;
              width: 24px;
              height: 24px;
              line-height: 60px;
              padding-bottom:1px;
              box-sizing: border-box; 
            }
        };
        };
</style>