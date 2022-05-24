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
    <br />
    <div class="vfor">
      <div class="for-box" v-for="(item, index) in list" :key="index">
        <div class="avatar"></div>
        <p class="small" v-text="item.text"></p>
      </div>
    </div>
    <div class="max-box">
      <div class="text-center">get commission</div>
      <div class="row">
        <div class="max-width" v-for="(item, index) in arr" :key="index">
          <div class="margin">
            <div class="card">
              <h5 class="font-weight">${{ item.money }}</h5>
              <p class="text-secondary" v-text="item.text"></p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="rowx">
      <a class="link" href="" v-for="(item, index) in array" :key="index">
        <img class="icon-png" :src="item.img" alt="" />
        {{ item.text }}
      </a>
    </div>
    <div class="item">
      <h6 class="subtitle">Membership level</h6>
      <div
        class="bg-template"
        v-for="(item, index) in home_list"
        :key="index">
        <div class="card-body">
          <div class="min-item">
            <div class="col-auto">
              <img src="../../assets/scheme.png" alt="" />
            </div>
            <div class="align-self-center">
              <h5 class="font-weight-normal">
                <span class="h5-left" v-text="item.title"></span>
                <span
                  v-bind:class="item.status == 1 ? 'h5-left' : ''"
                  class="h5-right"
                  >{{ item.status == 1 ? "Current level" : "Join>>" }}</span
                >
              </h5>
              <p class="text-mute" style="font-size: 12px; text-align: left">
                Minimum balance ${{ item.balance }}
              </p>
              <p class="text-mute" style="font-size: 12px; text-align: left">
                commission {{ item.commission }}% | {{ item.order }} Order
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="foot-title">Partner</div>
      <div class="foot-box">
        <img class="foot-img"  v-for="(item,index) in img_list" :key="index" :src="item.img" alt="">
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
      list: [],
      arr: [],
      array: [],
      home_list: [],
      img_list:[],
    };
  },
  created() {
    const list = [
      {
        text: "Team reports",
      },
      {
        text: "Topup",
      },
      {
        text: "Withdrawal",
      },
      {
        text: "Invitation",
      },
    ];
    const arr = [
      {
        money: "2109.13",
        text: "Today's earnings",
      },
      {
        money: "2109.13",
        text: "Today commission",
      },
      {
        money: "2109.13",
        text: "get commission",
      },
      {
        money: "0",
        text: "Yuebao",
      },
    ];
    const array = [
      {
        img: require("../../assets/link1.png"),
        text: "COMPANY INTRODUCTION",
      },
      {
        img: require("../../assets/link2.png"),
        text: "RULES DESCRIPTION",
      },
      {
        img: require("../../assets/link3.png"),
        text: "AGENT COOPERATION",
      },
      {
        img: require("../../assets/link4.png"),
        text: "COMPANY QUALIFICATION",
      },
    ];
    const home_list = [
      {
        balance: "0.00",
        commission: "0.23",
        order: "30",
        background: require("../../assets/vip-bg.png"),
        status: "1",
        background_color:
          "linear-gradient(240deg, rgb(12, 36, 66), rgb(79, 116, 146))",
        title: "VIP0",
      },
      {
        balance: "50.00",
        commission: "0.23",
        order: "50",
        background: require("../../assets/vip-bg.png"),
        status: "0",
        background_color:
          "linear-gradient(240deg, rgb(89, 112, 149), rgb(118, 138, 170))",
        title: "VIP1",
      },
      {
        balance: "300.00",
        commission: "0.28",
        order: "60",
        background: require("../../assets/vip-bg.png"),
        status: "0",
        background_color:
          "linear-gradient(240deg, rgba(219, 111, 33, 0.99), rgb(249, 153, 5))",
        title: "VIP2",
      },
      {
        balance: "1000.00",
        commission: "0.35",
        order: "70",
        background: require("../../assets/vip-bg.png"),
        status: "0",
        background_color:
          "linear-gradient(240deg, rgba(39, 53, 131, 0.99), rgb(47, 67, 177))",
        title: "VIP3",
      },
      {
        balance: "5000.00",
        commission: "0.45",
        order: "80",
        background: require("../../assets/vip-bg.png"),
        status: "0",
        background_color:
          "linear-gradient(240deg, rgba(61, 147, 181, 0.99), rgb(49, 179, 139))",
        title: "VIP4",
      },
      {
        balance: "10000.00",
        commission: "0.55",
        order: "90",
        background: require("../../assets/vip-bg.png"),
        status: "0",
        background_color:
          "linear-gradient(240deg, rgba(33, 35, 39, 0.99), rgb(67, 69, 73))",
        title: "VIP5",
      },
    ];
    const img_list = [
      {
        img:require('../../assets/amazon.png')
      },
      {
        img:require('../../assets/ebay.png')
      },
      {
        img:require('../../assets/bukalapak.png')
      },
      {
        img:require('../../assets/lazada.png')
      },
      {
        img:require('../../assets/walmart.png')
      },
      {
        img:require('../../assets/JB_Hi-Fi.png')
      },
      {
        img:require('../../assets/shopbot.png')
      },
      {
        img:require('../../assets/orami.png')
      },
    ];
    this.img_list = img_list
    this.home_list = home_list;
    this.list = list;
    this.arr = arr;
    this.array = array;
  },
  methods: {},
  mounted() {},
};
</script>

<style scoped lang="scss">
.Home {
  background: linear-gradient(to bottom, #fcedff 0%, #ffffff 100%);
  margin-bottom: 80px;
  .text-mute {
    opacity: 0.7;
    line-height: 22px;
  }
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
      .icon {
        color: #fff;
        font-size: 24px;
      }
      .btn-text {
        text-transform: uppercase;
        padding-top: 5px;
      }
    }
  }
  .vfor {
    width: 100%;
    height: 109px;
    padding: 0 15px;
    box-sizing: border-box;
    display: flex;
    justify-content: space-between;
    .for-box {
      width: auto;
      text-align: center;
      padding: 0 15px;
      .avatar {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        background: linear-gradient(135deg, #a700ff 0%, #00189a 100%);
        opacity: 0.3;
        margin: 0 auto;
      }
      .small {
        font-size: 12px;
        margin-top: 8px;
        color: #000;
      }
    }
  }
  .max-box {
    .text-center {
      font-size: 16px;
      margin-top: 30px;
      line-height: 26px;
      color: #333;
      text-transform: uppercase;
      margin-bottom: 0.25rem !important;
    }
    .row {
      display: flex;
      flex-wrap: wrap;
      .max-width {
        max-width: 50%;
        flex: 0 0 42.7%;
        padding: 0 15px;
        .margin {
          margin-bottom: 1rem !important;
          .card {
            box-shadow: 0 0.3rem 0.6rem rgb(0 0 0 / 10%) !important;
            border-radius: 10px;
            padding: 15px;
            box-sizing: border;
            .font-weight {
              font-weight: 400 !important;
              font-size: 20px;
            }
            .text-secondary {
              color: #666 !important;
              opacity: 0.7;
              font-size: 80%;
            }
          }
        }
      }
    }
  }
  .rowx {
    display: flex;
    flex-wrap: wrap;
    .link {
      text-align: center;
      text-decoration: none;
      flex: 0 0 25%;
      max-width: 25%;
      font-size: 12px;
      color: #6d00be;
      display: block;
      .icon-png {
        display: block;
        width: 73px;
        margin: 0 auto;
      }
    }
  }
  .item {
    padding: 0 15px;
    box-sizing: border-box;
    .subtitle {
      font-size: 16px;
      line-height: 26px;
      margin-top: 30px;
      margin-bottom: 15px;
      text-transform: uppercase;
      text-align: left;
      font-weight: 400;
    }
    .bg-template {
      margin-bottom: 1rem !important;
      border-radius: 10px;
      background: url("../../assets/vip-bg.png") center center / 160px 64px no-repeat,linear-gradient(240deg, rgb(12, 36, 66), rgb(79, 116, 146));
      &:nth-child(1n) {
        background:  url("../../assets/vip-bg.png") center center / 160px 64px no-repeat,linear-gradient(240deg, rgb(12, 36, 66), rgb(79, 116, 146));
      }
      &:nth-child(2n) {
        background:  url("../../assets/vip-bg.png") center center / 160px 64px no-repeat,linear-gradient(240deg, rgb(89, 112, 149), rgb(118, 138, 170));
      }
      &:nth-child(3n) {
        background:  url("../../assets/vip-bg.png") center center / 160px 64px no-repeat,linear-gradient(240deg, rgba(219, 111, 33, 0.99), rgb(249, 153, 5));
      }
      &:nth-child(4n) {
        background:  url("../../assets/vip-bg.png") center center / 160px 64px no-repeat,linear-gradient(240deg, rgba(61, 147, 181, 0.99), rgb(49, 179, 139));
      }
      &:nth-child(5n) {
        background:  url("../../assets/vip-bg.png") center center / 160px 64px no-repeat,linear-gradient(240deg, rgba(33, 35, 39, 0.99), rgb(67, 69, 73));
      }
      .card-body {
        padding: 15px;
        box-sizing: border-box;
        flex: 1 1 auto;
        .min-item {
          display: flex;
          flex-wrap: wrap;
          justify-content: space-between;
          .align-self-center {
            padding-left: 15px;
            flex-grow: 1;
            flex-basis: 0;
            max-width: 100%;
            color: #fff;
            .font-weight-normal {
              display: flex;
              justify-content: space-between;
              align-content: center;
              .h5-left {
                font-size: 20px !important;
                color: #fff !important;
              }
              .h5-right {
                font-size: 20px;
                color: #6d00be;
              }
            }
          }
        }
      }
    }
  }
  .footer{
    .foot-title {
      font-size: 16px;
      line-height: 26px;
      margin-top: 30px;
      margin-bottom: 10px;
      text-transform: uppercase;
      text-align: center;
      font-weight: 400;
    }
    .foot-box{
      display: flex;
      flex-wrap: wrap;
      .foot-img{
        flex: 0 0 24.3%;
        margin-top: 5px;
        width: 24.3%;
        height: 100px;
        margin-right: 2px;
      }
    }
  }
  .top-50 {
    margin-top: -50px;
    margin-bottom: 24px;
  }
}
</style>
