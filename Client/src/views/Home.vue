<template>
  <div class="bg">
    <div class="left">
      left
    </div>
    <div class="mid">
      <div class="box">
        <div class="title">
          留言區
        </div>
        123
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
        .title {
        background-color: #f1cb85;
        width: 256px;
        height: 48px;
        position: absolute;
        top: -40px;
        left: 20px;
        color: $fontColor;
        font-weight: bold;
        font-size: 36px;
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

