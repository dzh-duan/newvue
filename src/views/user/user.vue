<template>
  <div class="user">
    <div class="top">
          <div class="right">111111</div>
      <img src="../../assets/toxiang.png" alt="" />
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
.top {
  width: 345px;
  height: 190px;
  background-color: #a700ff;
  background: -webkit-linear-gradient(-45deg, #a700ff 0%, #00189a 100%);
  background: linear-gradient(135deg, #a700ff 0%, #00189a 100%);
  padding: 15px;
  box-sizing: border-box;
  display: flex;
  flex-direction: row-reverse;
  img {
    display: inline-block;
    background-color: #fff;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    line-height: 56px;
    vertical-align: middle;
    border-radius: 200px;
    display: inline-block;
    margin: 0px auto;
    background-color: #ffffff;
    overflow: hidden;
    text-align: center;
    

  }
}
</style>