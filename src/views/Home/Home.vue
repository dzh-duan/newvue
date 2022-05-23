<template>
    <div class="Home">
     <img class="img" src="../../assets/index.jpg" alt=""/>
     <!-- <div class="img"></div> -->
     <div class="container top-50">
       <div class="col">
         <h3 class="mb-0">$30.00</h3>
         <p class="text-mute">My balance</p>
       </div>
       <div class="col-auto">
         <button class="btn">
           <img class="money-png" src="../../assets/money.png" alt="">
         </button>
       </div>
       <div class="col-auto"></div>
     </div>
    </div>
</template>

<script>
export default {
  name: 'Home',
  components: {},
  data () {
    return {}
  },
  created () {
  },
  methods: {},
  mounted () {
  }
}
</script>

<style scoped lang="scss">
  .img{
    width: 100%;
    height: 280px;
    // background-color: black;
    display: block;
  }
  .container{
    width: 384px;
    height: 90px;
    padding: 15px;
    margin: 0 auto;
    // background-color: blue;
    background: #fff;
    z-index: 2;
    position: relative;
    box-sizing: border-box;
    border-radius: 10px;
    box-shadow: 5px 5px 5px #eee;
    display: flex;
    flex-wrap: wrap;
    .col{
      width: 186px;
      text-align: left;
      .mb-0{
        font-size: 30px;
        font-weight: 400;
      }
      .text-mute{
        opacity: 0.7;
      }
    }
    .col-auto{
      width: 54px;
      height: 54px;
      background-color: #6d00be;
      margin: 0 15px;
      .money-png{
        width: 24px;
        height: 24px;
        display: block;
      }
    }
  }
  .top-50{
    margin-top:-50px;
  }
  
</style>
