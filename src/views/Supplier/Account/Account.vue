<template>
  <div class="account">

    <el-card class="box-card">
      <div class="card-one">
        <div class="ico">
          <img :src="fire.ico" alt="">
        </div>
        <div class="msg" style="display">
          <p v-text="fire.name"></p>
          <p>供应商编码：
            <span v-text="fire.num"></span>
          </p>
          <p>业务类型：
            <span v-text="fire.type"></span>
          </p>
        </div>
        <div class="menu">
          <el-badge v-for="item in menus" :value="item.num" class="item">
            <span @click="toRouter(item.path)">
              <img :src="item.src" alt="">
              <p>{{item.num}}</p>
              <p>{{item.intro}}</p>
            </span>
          </el-badge>
        </div>
      </div>
    </el-card>

    <div class="card-two">
      <el-card>
        <div class="triangle"><span class="text">账号信息</span></div>
        <div class="info">
          <p v-for="(item,key) of account">
            <span class="info-font" v-text="item.name+':'"></span>
            <span class="content" v-text="item.value"></span>
            <el-button type="info" @click="alter(key)" v-if="item.alter">修改</el-button>
          </p>
        </div>
      </el-card>
      <el-card>
        <div class="triangle"><span class="text">账号信息</span></div>
        <div class="server">
          <p>
            <span class="info-font">结算方式：</span>{{info.way}}
          </p>
          <p>
            <span class="info-font">服务范围：</span>
            <el-tag v-for="item in info.range" type="info">{{item}}</el-tag>
          </p>
          <div class="pos">
            <h4>
              <span class="info-font">服务项</span>{{info.project}}
            </h4>
            <div class="menu">
              <ul>
                <li v-for="item in servers" @click="toRouter(item.path)">
                  <span class="note" v-text="item.note"></span>
                  <div class="wrap"><img :src="item.src" alt=""></div>
                  <p v-text="item.intro"></p>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </el-card>
    </div>



    <el-dialog title="会员信息修改" :visible.sync="dialogFormVisible">
      <el-form>
        <el-form-item :label="'请输入新的'+account[dialogType].name">
          <el-input auto-complete="off"></el-input>
        </el-form-item>
      </el-form>
      <div slot="footer" class="dialog-footer">
        <el-button @click="dialogChange">取 消</el-button>
        <el-button type="primary" @click="dialogChange">确 定</el-button>
      </div>
    </el-dialog>



  </div>
</template>
<script>
export default {
  data() {
    return {
      dialogFormVisible: false,
      dialogType: "email",
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
          intro: "待接单",
          path: "/"
        },
        {
          src: require("@/assets/account_icon2.png"),
          num: 2,
          intro: "待收货",
          path: "/"
        },
        {
          src: require("@/assets/account_icon3.png"),
          num: 0,
          intro: "运输中",
          path: "/"
        },
        {
          src: require("@/assets/account_icon4.png"),
          num: 0,
          intro: "已完成",
          path: "/"
        }
      ],
      account: {
        code: {
          name: "会员编码",
          value: "HH00001"
        },
        id: {
          name: "会员账号",
          value: "YOYO2017"
        },
        password: {
          name: "会员密码",
          value: "HH00001",
          alter: true
        },
        tel: {
          name: "手机号",
          value: "13900000000",
          alter: true
        },
        email: {
          name: "邮箱",
          value: "123456@qq.com",
          alter: true
        },
        type: {
          name: "账户类别",
          value: ""
        },
        power: {
          name: "账户级别",
          value: ""
        }
      },
      info: {
        way: "月结",
        range: ["深圳市", "上海市"],
        project: ""
      },
      servers: [
        {
          src: require("@/assets/detail_info_img1.png"),
          intro: "航空运输服务",
          note: "A",
          path: "/"
        },
        {
          src: require("@/assets/detail_info_img2.png"),
          intro: "航空运输服务",
          note: "B",
          path: "/"
        },
        {
          src: require("@/assets/detail_info_img3.png"),
          intro: "航空运输服务",
          note: "B",
          path: "/"
        },
        {
          src: require("@/assets/detail_info_img4.png"),
          intro: "航空运输服务",
          note: "D",
          path: "/"
        },
        {
          src: require("@/assets/detail_info_img5.png"),
          intro: "航空运输服务",
          note: "E",
          path: "/"
        }
      ]
    };
  },
  methods: {
    toRouter(path) {
      this.$router.push(path);
    },
    alter(type) {
      this.dialogType = type;
      this.dialogFormVisible = true;
    },
    dialogChange() {
      this.dialogFormVisible = false;
    }
  }
};
</script>
<style lang="scss" scoped>
@mixin font {
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

.account {
  $orange: #fccf00;
  margin-top: 61px + 30px;
  margin-left: 25px;
  display: flex;
  flex-direction: column;
  @mixin card {
    width: 100%;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
  .card-one {
    @include card;
    justify-content: space-around;
    align-items: center;
    padding: 15px 0;
    .msg {
      width: 400px;
      line-height: 40px;
    }
    .menu {
      width: 400px;
      span {
        display: inline-block;
        padding: 10px;
        cursor: pointer;
      }
      p {
        text-align: center;
      }
    }
  }

  .card-two {
    @include card;
    margin-top: 40px;
    justify-content: space-between;
    .triangle {
      position: absolute;
      width: 0;
      height: 0;
      border-top: 80px solid $orange;
      border-right: 80px solid transparent;
      .text {
        position: absolute;
        width: 100px;
        transform-origin: left top;
        transform: rotate(-45deg) translate(28%, -125%);
        color: white;
        font-size: 14px;
      }
    }

    $all-width: 1100px;
    $info-width: 650px;
    .info {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      width: $info-width;
      padding-left: 60px;
      .content {
        display: inline-block;
        width: 150px;
      }
    }
    $paddingLeft: 60px;
    .server {
      width: $all-width - $info-width;
      padding-left: $paddingLeft;
      h4 {
        text-align: center;
      }
      .menu {
        ul {
          padding: 0;
        }
        li {
          position: relative;
          display: inline-block;
          text-align: center;
          padding: 10px;
          cursor: pointer;
          .wrap {
            height: 45px;
          }
        }
      }
      .note {
        position: absolute;
        right: 0;
        top: 0;
      }
    }
    .info,
    .server {
      padding-top: 12px;
      .info-font {
        @include font;
      }
      .pos {
        margin-left: -$paddingLeft + 20;
      }
    }
  }
}
</style>
<style lang="scss">
$gray: #909399;
.account .el-card {
  border: 0;
  font-size: 15px;
  color: #a0a0a0;
  box-shadow: 0 8px 7px -5px rgba(0, 0, 0, 0.2);
  -webkit-box-shadow: 0 8px 7px -5px rgba(0, 0, 0, 0.2);
}

.account .el-button--info {
  color: #fff;
  background-color: $gray;
  border-color: $gray;
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
  $tagHeight: 20px;
  padding: 0 10px;
  height: $tagHeight+1;
  line-height: $tagHeight;
  font-size: 12px;
  margin-right: 8px;
  border-radius: 4px;
  box-sizing: border-box;
  border-color: $gray;
  color: $gray;
}

.account .el-card__body {
  padding: 0;
}
</style>
