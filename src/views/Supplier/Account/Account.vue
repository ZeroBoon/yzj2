<template>
  <div class="account">

    <el-card class="box-card">
      <div class="card-one">
        <div class="ico">
          <img src="../../../assets/head_img.png" alt="">
        </div>
        <div class="msg" style="display">
          <p>海航速运（北京）优先责任公司</p>
          <p>供应商编码：YZJ271939392900101</p>
          <p>业务类型：直营</p>
        </div>
        <div class="menu">
          <span>
            <img src="../../../assets/account_icon1.png" alt="">
            <p>0</p>
            <p>待接单</p>
          </span>
          <span>
            <img src="../../../assets/account_icon2.png" alt="">
            <p>0</p>
            <p>待收货</p>
          </span>
          <span>
            <img src="../../../assets/account_icon3.png" alt="">
            <p>2</p>
            <p>运输中</p>
          </span>
          <span>
            <img src="../../../assets/account_icon4.png" alt="">
            <p>0</p>
            <p>已完成</p>
          </span>
        </div>
      </div>
    </el-card>

    <div class="card-two">
      <el-card class="box-card">
        <div class="info">
          <p><span class="info-font">会员编码：</span><span class="content">{{account.code}}</span></p>
          <p><span class="info-font">会员账号：</span><span class="content">{{account.id}}</span></p>
          <p><span class="info-font">会员密码：</span><span class="content" v-if="account.password">{{account.password}}</span><el-button type="info">修改</el-button></p>
          <p><span class="info-font">手机号：</span><span class="content">{{account.tel}}</span><el-button type="info">修改</el-button></p>
          <p><span class="info-font">邮箱：</span><span class="content">{{account.email}}</span><el-button type="info">修改</el-button></p>
          <p><span class="info-font">账户类别：</span><span class="content">{{account.type}}</span></p>
          <p><span class="info-font">账户级别：</span><span class="content">{{account.power}}</span></p>
        </div>
      </el-card>
      <el-card class="box-card">
        <div class="server">
          <p><span class="info-font">结算方式：</span>{{info.way}}</p>
          <p><span class="info-font">服务范围：</span>{{info.range}}</p>
          <h4><span class="info-font">服务项</span>{{info.project}}</h4>
          <div class="menu">
            <span>
              <img src="../../../assets/detail_info_img1.png" alt="">
              <p>航空运输服务</p>
            </span>
            <span>
              <img src="../../../assets/detail_info_img2.png" alt="">
              <p>航空运输服务</p>
            </span>
            <span>
              <img src="../../../assets/detail_info_img3.png" alt="">
              <p>航空运输服务</p>
            </span>
            <span>
              <img src="../../../assets/detail_info_img4.png" alt="">
              <p>航空运输服务</p>
            </span>
            <span>
              <img src="../../../assets/detail_info_img5.png" alt="">
              <p>航空运输服务</p>
            </span>
          </div>
        </div>
      </el-card>
    </div>

  </div>
</template>
<script>
export default {
  data() {
    return {
      account: {
        code: "HH00001",
        id: "YOYO2017",
        password: "",
        tel: "13900000000",
        email: "123456@qq.com",
        type: "",
        power: ""
      },
      info: {
        way: "月结",
        range: "",
        project: ""
      }
    };
  }
};
</script>
<style lang="scss" scoped>
.account {
  $orange: #fccf00;

  margin-top: 61px + 30px;
  margin-left: 25px;
  display: flex;
  flex-direction: column;
  .card {
    width: 100%;
    height: 200px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
  .card-one {
    @extend .card;
    justify-content: space-around;
    align-items: center;
    .msg {
      width: 400px;
      line-height: 40px;
    }
    .menu {
      width: 400px;
      span {
        display: inline-block;
        padding: 10px;
      }
      p {
        text-align: center;
      }
    }
  }

  .card-two {
    @extend .card;
    margin-top: 40px;
    justify-content: space-between;
    .box-card {
      height: 380px;
      &::before {
        content: "";
        position: absolute;
        width: 0;
        height: 0;
        border-top: 60px solid $orange;
        border-right: 60px solid transparent;
      }
    }
    .font {
      display: inline-block;
      width: 110px;
      height: 18px;
      margin-right: 15px;
      text-align: justify;
      overflow: hidden;
      &::after {
        width: 100%;
        height: 0;
        margin: 0;
        display: inline-block;
        overflow: hidden;
        content: "";
      }
    }
    $all-width: 1100px;
    $info-width: 640px;
    .info {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      width: $info-width;
      padding-left: 40px;
      .info-font {
        @extend .font;
      }
      .content {
        display: inline-block;
        width: 150px;
      }
    }
    .server {
      width: $all-width - $info-width;
      padding-left: 20px;
      .info-font {
        @extend .font;
      }
      h4 {
        text-align: center;
      }
      .menu {
        span {
          display: inline-block;
          text-align: center;
          padding: 10px;
        }
      }
    }
  }
}
</style>
<style lang="scss">
.account .el-card {
  font-size: 15px;
  font-weight: bold;
  color: #ccc;
}
.account .el-button--info {
  color: #fff;
  background-color: #909399;
  border-color: #909399;
  width: 75px;
  padding: 1px;
}
</style>
