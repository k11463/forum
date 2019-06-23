<template>
  <div class="bg">
    <div class="left">
      left
    </div>
    <div class="mid">
      <div class="box">
        <div class="title">
          討論區
        </div>
        <div class="contents">
          <div class="content" v-for="i in 10" :key="i">
            {{ i }}號失蹤榮
          </div>
        </div>
      </div>
    </div>
    <div class="right">
      right
    </div>
  </div>
</template>

<script>
  export default {
    components: {
      
    }
  }
</script>

<style lang="scss" scoped>
$fontColor: rgb(255, 245, 203);
.bg {
  width: 100vw;
  height: 120vh;
  background-color: rgb(241, 234, 223);
  font-family: "標楷體";
  margin-top: 6vh;
  .left {
    width: 15%;
    height: 100%;
    float: left;
  }
  .mid {
    width: 69%;
    height: 100%;
    padding: 20px;
    padding-top: 80px;
    float: left;
    .box {
        height: 768px;
        background-color: #fff;
        border-radius: 8px;
        position: relative;
        border-radius: 8px;
        .title {
          background-color: #f1cb85;
          width: 12%;
          height: 6%;
          position: absolute;
          top: -32px;
          left: 20px;
          color: $fontColor;
          font-weight: bold;
          font-size: 36px;
          border-radius: 8px;
          display: flex;
          align-items: center;
          justify-content: center;
          letter-spacing: 8px;  
        }
        .contents {
          width: 100%;
          height: 100%;
          padding: 20px;
          padding-top: 36px;
          .content {
            border: 1px solid #f1cb85;
            width: 100%;
            height: 10%;
            border-radius: 4px;
          }
          .content:hover {
            background-color: #ffeac4;
            border: 1px solid rgb(255, 196, 0);
            cursor: pointer;
          }
        }
    }
  }
  .right {
    width: 15%;
    height: 100%;
    float: left;
  }
}
</style>

