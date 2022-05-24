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
      <div></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "user",
  components: {},
  data() {
    return {};
  },
  created() {},
  methods: {},
  mounted() {},
};
</script>

<style scoped lang="scss">
.user {
  .top {
    box-sizing: border-box;
    margin: 54px auto 0;
    border-radius: 10px;
    width: 345px;
    height: 190px;
    background-color: #a700ff;
    background: -webkit-linear-gradient(-45deg, #a700ff 0%, #00189a 100%);
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
    margin: -100px auto 0;
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
      .colit{
        padding: 0 15px;
        width: 109.5px;
        display: inline-block;
      }
    }
  }
}
</style>