<template>
  <div class="user">
    <div class="top">
      <img class="tup2" src="../../assets/toxiang.png" alt="" />
      <div class="right">
        <h5>1890000999 &nbsp;<span>VIP0</span></h5>
        <div class="shanzi">
          <span class="ziti">Invitation code </span>
          <i>&nbsp;946375</i>
          <img class="tup" src="../../assets/lihe.png" alt="" />
        </div>
      </div>
    </div>
    <div class="center">
      <div class="top2">
        <div class="dahezi">
          <h3>$30</h3>
          <p>
            Account <br />
            balance
          </p>
        </div>
        <div class="colit">
          <h3>$100</h3>
          <p>
            Account <br />
            balance
          </p>
        </div>
        <button class="jiahao">
          <img src="../../assets/jiahao.png" alt="" />
        </button>
      </div>
      <div class="caixukun">
        <div class="luhan">
          $30.00 <br />
          Available balance
        </div>
        <div class="huangzitao">$0.00 <br />Frozen amount</div>
      </div>
    </div>
    <div class="buttom">
      <div class="dalizi">
        <div class="jianto" v-for="(b, index) in list" :key="index">
          <div class="duanzhihui" :class="b.status==1?'background':''">
            <img class="spang" :src="b.img" alt="">
          </div>
          <div class="xiaofangkuai">
            <h4 class="xiaofangkuai-left">{{ b.name }}</h4>
            <img class="material-icons" src="../../assets/arrow-right.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "user",
  components: {},
  data() {
    return {
      list: [
        {
          name: "Withdrawal",
          img:require("../../assets/youshangjianto.png"),
          status:'0'
        },
        {
          name: "Team reports",
          img:require("../../assets/yonghuzu.png"),
          status:'0'
        },
        {
          name: "recharge record",
          img:require("../../assets/heijiahao.png"),
          status:'0'
        },
        {
          name: "Withdrawal record",
          img:require("../../assets/zhaoxiangji.png"),
          status:'0'
        },
        {
          name: "Personal data",
          img:require("../../assets/xunhuan.png"),
          status:'0'
        },
        {
          name: "Announcement",
          img:require("../../assets/tixing.png"),
          status:'0'
        },
        {
          name: "Shopping address",
          img:require("../../assets/xingyongka.png"),
          status:'0'
        },
        {
          name: "Binding Bank card",
          img:require("../../assets/xingyongka.png"),
          status:'0'
        },
        {
          name: "Change Password",
          img:require("../../assets/jiesuo.png"),
          status:'0'
        },
        {
          name: "Finacial",
          img:require("../../assets/gupiao.png"),
          status:'0'
        },
        {
          name: "Language",
          img:require("../../assets/diqiu.png"),
          status:'0'
        },
        {
          name: "Logout",
          img:require("../../assets/qidong.png"),
          status:'1'
        },
      ],
    };
  },
  created() {},
  methods: {},
  mounted() {},
};
</script>

<style scoped lang="scss">
.user {
  margin-bottom: 80px;
  padding-top: 54px;
  box-sizing: border-box;
  background: linear-gradient(to bottom, #fcedff 0%, #ffffff 100%);
  .top {
    box-sizing: border-box;
    margin: 0 auto;
    border-radius: 10px;
    width: 345px;
    height: 190px;
    background: linear-gradient(135deg, #a700ff 0%, #00189a 100%);
    padding: 15px;

    display: flex;
    flex-direction: row;
    .tup2 {
      display: inline-block;
      background-color: #fff;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      line-height: 56px;
      margin: 0 10px;
      box-sizing: border-box;
    }
    .right {
      width: 191px;
      height: 50px;
      color: #fff;
      .shanzi {
        text-align: left;
        display: flex;
        align-items: center;
      }
      .ziti {
        font-size: 12.8px;
        opacity: 0.7;
      }
      h5 {
        font-size: 20px;
        text-align: left;
        margin-bottom: 4px;
        span {
          font-size: 16px;
        }
      }
      i {
        opacity: 0.7;
        font-style: normal;
        font-size: 12.8px;
      }
      .tup {
        width: 18px;
        height: 18px;
        box-sizing: border-box;
        background-size: 100% 100%;
        margin-left: 15px;
      }
    }
  }
  .center {
    width: 345px;
    height: 180px;
    margin-top: -100px;
    background: #fff;
    margin: -100px auto 24px;
    border-radius: 10px;
    box-shadow: 0 0.3rem 0.6rem rgb(0 0 0 / 10%);
    .top2 {
      text-align: left;
      border-bottom: 1px solid #dee2e6;
      padding: 15px;

      .dahezi {
        width: 109.5px;
        display: inline-block;
      }
      h3 {
        font-size: 30px;
        font-weight: 400;
        display: inline-block;
        width: 109.5px;
      }
      p {
        color: #666666;
        width: 109.5px;
        display: inline-block;
        font-size: 20px;
        display: inline-block;
      }
      .jiahao {
        height: 54px;
        width: 54px;
        border-radius: 50%;
        position: absolute;
        right: 20px;
        background-color: #6d00be;
        border: none;
        align-items: center;
        padding: 15px;
        img {
          width: 18px;
          height: 18px;
        }
      }
      .colit {
        padding: 0 15px;
        width: 109.5px;
        display: inline-block;
      }
    }
    .caixukun {
      width: 345px;
      height: 69px;
      box-sizing: border-box;
      padding: 15px;
      display: flex;
      justify-content: space-between;
      .luhan {
        display: inline-block;
      }
      .huangzitao {
        display: inline-block;
      }
    }
  }
  .buttom {
    padding: 0 15px;
    box-sizing: border-box;
   
    
    .dalizi {
       border-radius: 10px;
      background-color: #fff;
      box-shadow: 0 0.3rem 0.6rem rgb(0 0 0 / 30%);
      padding: 15px 0;
      .jianto {
        &:last-of-type{
          border: none;
          
        }
        padding: 15px;
        box-sizing: border-box;
        display: flex;
        align-items: center;
        // background-color: #6d00be;
        
        border-bottom: 1px solid rgba(0, 0, 0, 0.125);
        .duanzhihui {
          width: 50px;
          height: 50px;
          background: linear-gradient(135deg, #a700ff 0%, #00189a 100%);
          opacity: 0.3;
          margin-right: 15px;
          border-radius: 10px;
          box-shadow: 0 5px 10px rgb(0 0 0 / 30%);
          display: flex;
          align-items: center;
          justify-content: center;
          .spang{
            display: inline-block;
            width: 24px;
            height: 24px;
          }
        }
        .background{
          background: #fff !important;
        }
        .xiaofangkuai {
          flex: 1;
          margin: 0 auto;
          display: inline-block;
          display: flex;
          align-items: center;
          justify-content: space-between;
          .xiaofangkuai-left{
            font-size: 16px;
            color: #6d00be;
            font-weight: 500;
          }
          .material-icons {
            width: 24px;
            height: 24px;
            display: block;
          }
          h4 {
          }
        }
      }
    }
  }
}
</style>