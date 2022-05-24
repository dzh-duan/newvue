<template>
  <div class="pay">
    <div class="top">
      <div class="dahezi">
        <h3>${{ money }}</h3>
        <p>Account Funds</p>
      </div>
      <button class="jiahao">
        <img src="../../assets/jiahao.png" alt="" />
      </button>
    </div>
    <div class="bottom">
      <div class="jianbian">
        <h3>Free</h3>
        <h5>Investment amount $0.00</h5>
        <p>commission&nbsp;0% | 30&nbsp;Order</p>
        <span><i>0</i>/30</span>
      </div>
    </div>
    <div class="top_hezi">
      <div class="lihezi" v-for="(a,index) in list" :key="index">
        <i>{{a.status==3 ? '':'$'}}</i>{{a.title}} <br>
        <i>{{a.name}}</i>
      </div>
      <!-- <div class="lihezi2">
        ${{a.title}} <br>
        <i>{{a.name}}</i>
      </div> -->
    </div>
    <div class="changzi">
      <button>
        <span>Start grabbing orders</span>
      </button>
      
    </div>
    <div class="border"></div>
  </div>
</template>

<script>
export default {
  name: "pay",
  components: {},
  data() {
    return {
      money:"30.00",
      list:[
        {
          title:"0",
          name:"Get commission",
          status:"1"
        },
        {
          title:"0",
          name:"Frozen amount",
          status:"2"
        },
        {
          title:"0",
          name:"Order quantity",
          status:"3"
        },
        {
          title:"0",
          name:"Available balance",
          status:"4"
        },
      ]
    };
  },
  created() {},
  methods: {},
  mounted() {

  },
};
</script>

<style scoped lang="scss">
.pay {
  height: 725px;
  width: 100%;
  padding-right: 15px;
  padding-left: 15px;
  padding-top: 54px;
  box-sizing: border-box;
  .top {
    text-align: left;
    display: flex;
    .dahezi {
      width: 261px;
    }
    h3 {
      font-size: 30px;
      font-weight: 400;
      display: inline-block;
      width: 261px;
    }
    p {
      color: #666666;
      width: 261px;
      display: inline-block;
    }
    .jiahao {
      height: 54px;
      width: 54px;
      padding: 0;
      border-radius: 50%;
      background-color: #6d00be;
      margin-left: 10px;
      border: none;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 15px;
      img {
        width: 18px;
        height: 18px;
      }
    }
  }
  .bottom {
    width: 345px;
    height: 200px;
    margin: 0 auto;
    margin-top: 46.8px;
    border-radius: 10px;
    background: linear-gradient(135deg, #a700ff 0%, #00189a 100%);
    .jianbian {
      color: #fff;
      h3 {
        text-align: left;
        padding: 15px 15px 10px;
        font-size: 30px;
      }
      h5 {
        font-size: 20px;
        text-align: left;
        margin-right: 8px;
        margin-left: 12px;

      }
      p {
        text-align: left;
        padding:5px 10px 15px;

      }
      span{
        font-size: 30px;
        i{
          font-style: normal;
          background: limegreen;
          padding: 0 5px;
        }
      }
    }
  }
  .top_hezi{
    display: flex;
    flex-wrap: wrap;
    border-bottom: 1px solid #dee2e6;
    padding-top:15px;
    
    .lihezi{
      width: 50%;
      height: 45px;
      border-bottom: 1px solid #dee2e6;
      display: inline-block;
      text-align: left;
      padding-top: 15px;
      font-size: 12.8px;

    &:nth-child(2n){
      text-align: right;
    }
    }
      // .lihezi2{
      //   width: 142.5px;
      //   height: 45px;
      //   display: inline-block;
      //   text-align: right;
      //   margin-right: 15px;
      // }
  }
  .changzi{
    padding: 12px 15px;
    border-bottom: 1px solid #dee2e6;
    button{
      background-color: #6d00be;
      width: 315px;
      height: 50px;
      border: none;
      border-radius: 30px;
      span{
        color: #fff;
        font-size: 16px;
        text-transform: uppercase;
      }
    }
  }
  .border{
    border-bottom: 1px solid #dee2e6;
      width: 315px;
      height: 50px;
      border: none;
      border-radius: 30px;
      margin: 0 auto;
      box-sizing: border-box;
  }
}
</style>