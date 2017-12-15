<template>
  <div class="account">

    <el-card class="box-card">
      <div class="card-one">
        <div class="ico">
          <img :src="fire.ico" alt="">
        </div>
        <div class="msg" style="display">
          <p v-text="fire.name"></p>
          <p>供应商编码：<span v-text="fire.num"></span></p>
          <p>业务类型：<span v-text="fire.type"></span></p>
        </div>
        <div class="menu">
          <el-badge v-for="item in menus" :value="item.num" class="item">
              <span>
                <img :src="item.src" alt="">
                <p>{{item.num}}</p>
                <p>{{item.intro}}</p>
              </span>
          </el-badge>
        </div>
      </div>
    </el-card>

    <div class="card-two">
      <el-card class="box-card">
        <div class="info">
          <p><span class="info-font">会员编码：</span><span class="content" v-text="account.code"></span></p>
          <p><span class="info-font">会员账号：</span><span class="content" v-text="account.id"></span></p>
          <p><span class="info-font">会员密码：</span><span class="content" v-if="account.password" v-text="account.password"></span><el-button type="info" @click="alter('password')">修改</el-button></p>
          <p><span class="info-font">手机号：</span><span class="content" v-text="account.tel"></span><el-button type="info" @click="alter('tel')">修改</el-button></p>
          <p><span class="info-font">邮箱：</span><span class="content" v-text="account.email"></span><el-button type="info" @click="alter('email')">修改</el-button></p>
          <p><span class="info-font">账户类别：</span><span class="content" v-text="account.type"></span></p>
          <p><span class="info-font">账户级别：</span><span class="content" v-text="account.power"></span></p>
        </div>
      </el-card>
      <el-card class="box-card">
        <div class="server">
          <p><span class="info-font">结算方式：</span>{{info.way}}</p>
          <p><span class="info-font">服务范围：</span><el-tag v-for="item in info.range" type="info">{{item}}</el-tag></p>
          <h4><span class="info-font">服务项</span>{{info.project}}</h4>
          <div class="menu">
            <span v-for="item in servers">
              <img :src="item.src" alt="">
              <p>{{item.intro}}</p>
            </span>
          </div>
        </div>
      </el-card>
    </div>





    <el-dialog title="信息修改" :visible.sync="dialogFormVisible">
      <el-form :model="account">
        <el-form-item label="活动名称" >
          <el-input auto-complete="off"></el-input>
        </el-form-item>
      </el-form>
      <div slot="footer" class="dialog-footer">
        <el-button @click="dialogFormVisible = false">取 消</el-button>
        <el-button type="primary" @click="dialogFormVisible = false">确 定</el-button>
      </div>
    </el-dialog>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dialogFormVisible: false,
      fire: {
        ico: require("../../../assets/head_img.png"),
        name: "海航速运（北京）优先责任公司",
        num: "YZJ271939392900101",
        type: "直营"
      },
      menus: [
        {
          src: require("@/assets/account_icon1.png"),
          num: 0,
          intro: "待接单"
        },
        {
          src: require("@/assets/account_icon2.png"),
          num: 2,
          intro: "待收货"
        },
        {
          src: require("@/assets/account_icon3.png"),
          num: 0,
          intro: "运输中"
        },
        {
          src: require("@/assets/account_icon4.png"),
          num: 0,
          intro: "已完成"
        }
      ],
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
        range: ["深圳市", "上海市"],
        project: ""
      },
      servers: [
        {
          src: require("@/assets/detail_info_img1.png"),
          intro: "航空运输服务"
        },
        {
          src: require("@/assets/detail_info_img2.png"),
          intro: "航空运输服务"
        },
        {
          src: require("@/assets/detail_info_img3.png"),
          intro: "航空运输服务"
        },
        {
          src: require("@/assets/detail_info_img4.png"),
          intro: "航空运输服务"
        },
        {
          src: require("@/assets/detail_info_img5.png"),
          intro: "航空运输服务"
        }
      ]
    };
  },
  methods: {
    alter(type) {
      this.dialogFormVisible = true;
    }
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
  color: #a0a0a0;
  box-shadow: 0 15px 25px -5px rgba(0, 0, 0, 0.1);
  -webkit-box-shadow: 0 15px 25px -5px rgba(0, 0, 0, 0.1);
}
.account .el-button--info {
  color: #fff;
  background-color: #909399;
  border-color: #909399;
  width: 75px;
  padding: 1px;
}

.account .el-badge__content.is-fixed {
  position: absolute;
  top: 15px;
  right: 25px;
  -webkit-transform: translateY(-50%) translateX(100%);
  transform: translateY(-50%) translateX(100%);
}

.account .el-tag {
  padding: 0 10px;
  height: 26px;
  line-height: 27px;
  font-size: 12px;
  margin-right: 8px;
  border-radius: 4px;
  box-sizing: border-box;
}
</style>
