<template>
  <div class="service">
    <div class="top">
      <p class="kefu">Customer service center</p>
      <p class="ruguo">If you need help with problems, please contact online</p>
    </div>
    <div class="bottom">
      <div class="xiaohezi">
        <div class="tp" v-for="(i,index) in list" :key="index">
          <p>
            {{i.title}}
            <img :src="i.img" alt="" />
          </p>
          <img class="tupian" :src="i.img2" alt="" />
          <span>
            <i v-text="i.time"></i>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "service",

  components: {},
  data() {
    return {
      list:[
        {
          title:"service 1",
          img: require("../../assets/kefu2.png"),
          img2: require("../../assets/kefu3.png"),
          time:"13:00-22:00"
        },
        {
          title:"service 2",
          img: require("../../assets/kefu2.png"),
          img2: require("../../assets/kefu3.png"),
          time:"13:00-22:00"
        },
        {
          title:"service 3",
          img: require("../../assets/kefu2.png"),
          img2: require("../../assets/kefu3.png"),
          time:"13:00-22:00"
        },
        {
          title:"service 4",
          img: require("../../assets/kefu2.png"),
          img2: require("../../assets/kefu3.png"),
          time:"13:00-22:00"
        },
        {
          title:"service 5",
          img: require("../../assets/kefu2.png"),
          img2: require("../../assets/kefu3.png"),
          time:"13:00-22:00"
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
.service {
  * {
    margin: 0;
    padding: 0;
    font-family: Microsoft YaHei;
  }
  .top {
    position: absolute;
    top: 0;
    left: 0;
    height: 177px;
    width: 100%;
    background-image: url("../../../src/assets/beijingtu.png");
    background-color: rgba(186, 195, 210);
    background-size: 100%;
    overflow-y: hidden;
    p {
      width: 339px;
      margin: 0 auto;
      text-align: left;
    }
    .kefu {
      padding-top: 17.5px;
      margin-bottom: 37.5px;
      font-size: 24px;
      font-weight: 600;
      color: #2f3848;
      font-family: Microsoft YaHei;
    }
    .ruguo {
      font-size: 11.84px;
      padding-top: 9px;
      font-family: Microsoft YaHei;
      color: rgba(47, 56, 72, 0.5);
    }
  }
  .bottom {
    width: 100%;
    background: #fff;
    z-index: 100;
    position: absolute;
    border-radius: 12px;
    top: 112.5px;
    .xiaohezi {
      margin-top: 53.5px;
      display: flex;
      flex-wrap: wrap;
      padding: 0 16px;
        box-sizing: border-box;
      .tp {
        width: 163.5px;
        height: 232.5px;
        background-color: #f6f7f7;
        margin: 8px 8px 8px 0;
        .tupian {
          display: inline-block;
          width: 20px;
          height: 20px;
          vertical-align: middle;
          margin-left: -85px;
        }
      }
      p {
        text-align: left;
        margin: 12px 0 8px;
        font-weight: 700;
        color: #434343;
        font-size: 14px;
        img {
          width: 139.5px;
          height: 79.98px;
        }
      }
      span {
        i {
          font-size: 12px;
        }
        display: inline-block;

        // width: ;
      }
    }
  }
}
</style>