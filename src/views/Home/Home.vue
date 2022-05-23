<template>
  <div class="Home">
    <img class="img" src="../../assets/index.jpg" alt="" />
    <!-- <div class="img"></div> -->
    <div class="container top-50">
      <div class="col">
        <h3 class="mb-0">$30.00</h3>
        <p class="text-mute">My balance</p>
      </div>
      <div class="col-auto">
        <button class="btn">
          <img class="money-png" src="../../assets/money.png" alt="" />
        </button>
      </div>
      <div class="col-auto">
        <button class="btn">
          <img class="money-png" src="../../assets/kefu.png" alt="" />
        </button>
      </div>
    </div>
    <div class="btn-block">
      <button class="button">
        <i class="icon iconfont icon-zuoyouhuadong"></i>
        <div class="btn-text">Start making money</div>
      </button>
    </div>
    <br>
    <div class="vfor">
      <div class="for-box" v-for="(item,index) in list" :key="index">
        <div class="avatar"></div>
        <p class="small" v-text="item.text"></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data() {
    return {
      list:[
        {
          text:"Team reports"
        },
        {
          text:"Topup"
        },
        {
          text:"Withdrawal"
        },
        {
          text:"Invitation"
        },
      ]
    };
  },
  created() {
    const list = []
    // this.list = list
  },
  methods: {},
  mounted() {},
};
</script>

<style scoped lang="scss">
.img {
  width: 100%;
  height: 280px;
  // background-color: black;
  display: block;
}
.container {
  width: 384px;
  height: 90px;
  padding: 15px 0;
  margin: 0 auto;
  // background-color: blue;
  background: #fff;
  z-index: 2;
  position: relative;
  box-sizing: border-box;
  border-radius: 10px;
  box-shadow: 0 0.3rem 0.6rem rgb(0 0 0 / 10%) !important;
  display: flex;
  flex-wrap: wrap;
  .col {
    width: 186px;
    text-align: left;
    margin: 0 15px;
    .mb-0 {
      font-size: 30px;
      font-weight: 400;
      line-height: 1.2;
    }
    .text-mute {
      opacity: 0.7;
      line-height: 22px;
    }
  }
  .col-auto {
    width: 54px;
    height: 54px;
    background-color: #6d00be;
    margin: 0 15px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-content: center;
    .btn {
      border: none;
      background: rgba(0, 0, 0, 0);
      .money-png {
        width: 24px;
        height: 24px;
        display: block;
      }
    }
  }
}
.btn-block {
  width: 384px;
  background-color: #6d00be;
  margin: 0 auto;
  border-radius: 30px;
  .button {
    width: 100%;
    height: 100%;
    border: none;
    background: rgba(0, 0, 0, 0);
    font-size: 16px;
    display: flex;
    color: #fff;
    align-content: center;
    justify-content: center;
    padding: 13px 24px;
    box-sizing: border-box;
    .icon{
      color: #fff;
      font-size: 24px;
    }
    .btn-text{
      text-transform: uppercase;
      padding-top: 5px;
    }
  }
}
.vfor{
  width: 100%;
  padding: 0 15px;
  box-sizing: border-box;
  display: flex;
  justify-content:space-between;
  .for-box{
    width: auto;
    text-align: center;
    padding: 0 15px;
    .avatar{
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background: linear-gradient(135deg, #a700ff 0%, #00189a 100%);
      opacity: 0.3;
      margin: 0 auto;
    }
    .small{
      font-size: 12px;
      margin-top: 8px;
      color: #000;
    }
  }
}
.top-50 {
  margin-top: -50px;
  margin-bottom: 24px;
}
</style>
