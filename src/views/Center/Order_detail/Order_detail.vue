<template>
  <div class="order_detail">
    <div class="head">
      <div class="title">
        <el-breadcrumb separator=">>>">
          <el-breadcrumb-item :to="{ path: '/center/order_search' }">订单查询</el-breadcrumb-item>
          <el-breadcrumb-item>订单详情</el-breadcrumb-item>
        </el-breadcrumb>
      </div>
    </div>
    <div class="main">
      <div class="main-top">
        <div class="linear"></div>
        <div class="main-top-title">
          <div class="time">2017-10-10 10:10:10</div>
          <div class="btn"><span class="reset">修改订单</span><span>|</span><span class="cancle">取消订单</span></div>
        </div>
        <div class="content">
          <div class="left">
            <div class="box orderNum">
              <div class="title">订单编号:</div>
              <div class="detail">46464646464164</div>
            </div>
            <div class="box transLine">
              <div class="title">运输线路:</div>
              <div class="detail">北京(PEK)——上海(PVG)</div>
            </div>
            <div class="box baseserve">
              <div class="title">基础服务:</div>
              <div class="detail">
                <div class="item"><span class="get el-icon-circle-check"></span><span>航空运输</span></div>
              </div>
            </div>
            <div class="box moreserver">
              <div class="title">更多服务:</div>
              <div class="detail">
                <div class="item"><span class="get el-icon-circle-check"></span><span>代交货</span></div>
                <div class="item"><span class="get el-icon-circle-check"></span><span>代提交</span></div>
                <div class="item"><span class="get el-icon-circle-check"></span><span>上门取货</span></div>
                <div class="item not"><span class="get el-icon-circle-check"></span><span>落地配</span></div>
              </div>
            </div>
            <div class="box increaseserver">
              <div class="title">增值服务:</div>
              <div class="detail">
                <div class="item"><span class="get el-icon-circle-check"></span><span>报关报检</span></div>
                <div class="item not"><span class="get el-icon-circle-check"></span><span>运输保险</span></div>
              </div>
            </div>
          </div>
          <div class="middle">
            <img src="../../../assets/send.png" alt="">
            <p>运送中</p>
          </div>
          <div class="right">
            <el-button type="danger" @click="goto('/center/order_track')">订单跟踪</el-button>
          </div>
        </div>
      </div>
      <div class="server-info">
        <div class="triangle">
            <div><span>服</span><span>务</span><span>信</span><span>息</span></div>
        </div>
        <div class="box airtrans">
          <div class="img"><img src="../../../assets/detail_info_img1.png" alt=""></div>
          <div class="title">航空运输服务</div>
          <div class="content">
            <div class="item flightNumber">
              <span>预定航班：</span><span>HU7211</span>
            </div>
            <div class="item flightData">
              <span>航班时间：</span><span>2017-10-10</span>
            </div>
            <div class="item flighttime">
              <span>航班时刻：</span><span>10:10</span>
            </div>
            <div class="item transNum">
              <span>运单号码：</span><span>80-135464</span>
            </div>
          </div>
        </div>
        <div class="box beginport">
          <div class="img"><img src="../../../assets/detail_info_img2.png" alt=""></div>
          <div class="title">始发港地面操作服务</div>
          <div class="content">
            <div class="item flightNumber">
              <span>最晚交货时间：</span><span>2017-10-10</span>
            </div>
            <div class="item flightData">
              <span>货运代理：</span><span>海航速运北京分公司</span>
            </div>
            <div class="item flighttime">
              <span>交货位置：</span><span>北京市朝阳区爱国路21号</span>
            </div>
            <div class="item transNum">
              <span>联系方式：</span><span>13468465435</span>
            </div>
          </div>
        </div>
        <div class="box endport">
          <div class="img"><img src="../../../assets/detail_info_img3.png" alt=""></div>
          <div class="title">目的港地面操作服务</div>
          <div class="content">
            <div class="item flightNumber">
              <span>预计取货时间：</span><span>2017-11-11</span>
            </div>
            <div class="item flightData">
              <span>货运代理：</span><span>海航速运北京分公司</span>
            </div>
            <div class="item flighttime">
              <span>交货位置：</span><span>北京市朝阳区爱国路21号</span>
            </div>
            <div class="item transNum">
              <span>联系方式：</span><span>15156556666</span>
            </div>
          </div>
        </div>
        <div class="box pickup ">
          <div class="img"><img src="../../../assets/detail_info_img4.png" alt=""></div>
          <div class="title">上门取货服务</div>
          <div class="content">
            <div class="item flightNumber">
              <span>预计取货时间：</span><span>2017-10-10</span>
            </div>
            <div class="item flightData">
              <span>货运代理：</span><span>海航速运北京分公司</span>
            </div>
            <div class="item flighttime">
              <span>运输方式：</span><span>专车配送</span>
            </div>
            <div class="item transNum">
              <span>运输车辆：</span><span>1吨金杯车</span>
            </div>
            <div class="item transNum">
              <span>取货位置：</span><span>北京市朝阳区爱国路21号</span>
            </div>
            <div class="item transNum">
              <span>联系方式:</span><span>13215645468</span>
            </div>
          </div>
        </div>
        <div class="box landing">
          <div class="img"><img src="../../../assets/detail_info_img5.png" alt=""></div>
          <div class="title">落地配服务</div>
          <div class="content">
            <div class="item flightNumber">
              <span>预计取货时间：</span><span>2017-10-10</span>
            </div>
            <div class="item flightData">
              <span>货运代理：</span><span>海航速运上海分公司</span>
            </div>
            <div class="item flighttime">
              <span>运输方式：</span><span>一般配送</span>
            </div>
            <div class="item transNum">
              <span>运输车辆：</span><span>5吨箱式火车</span>
            </div>
            <div class="item transNum">
              <span>取货位置：</span><span>上海市爱国区爱国路21号</span>
            </div>
            <div class="item transNum">
              <span>联系方式:</span><span>156465465645</span>
            </div>
          </div>
        </div>
        <div class="box more">
          <div>
            <img src="../../../assets/detail_info_imgmore.png" alt="">
          </div>
        </div>
      </div>
      <div class="address">
        <div class="center-icon">
          <img src="../../../assets/plane_icon.png" alt="">
        </div>
        <div class="triangle">
            <div><span>收</span><span>发</span><span>地</span><span>址</span></div>
        </div>
        <div class="left">
          <div class="icon">发</div>
          <div class="box name-id">
            <div class="key">姓名</div>
            <div class="value">陈悠悠</div>
            <div class="key">身份证</div>
            <div class="value">186431351654646644654</div>
          </div>
          <div class="box phone-cellphone">
            <div class="key">手机号</div>
            <div class="value">17655556666</div>
            <div class="key">固定电话</div>
            <div class="value">200-54646541</div>
          </div>
          <div class="box address-detial">
            <div class="key">详细地址</div>
            <div class="value">北京市朝阳区爱国路20号</div>
          </div>
          <div class="box postal">
            <div class="key">邮政编码</div>
            <div class="value">518100</div>
          </div>
        </div>
        <div class="right">
          <div class="icon">收</div>
          <div class="box name-id">
            <div class="key">姓名</div>
            <div class="value">陈悠悠</div>
            <div class="key">身份证</div>
            <div class="value">186431351654646644654</div>
          </div>
          <div class="box phone-cellphone">
            <div class="key">手机号</div>
            <div class="value">17655556666</div>
            <div class="key">固定电话</div>
            <div class="value">200-54646541</div>
          </div>
          <div class="box address-detial">
            <div class="key">详细地址</div>
            <div class="value">北京市朝阳区爱国路20号</div>
          </div>
          <div class="box postal">
            <div class="key">邮政编码</div>
            <div class="value">518100</div>
          </div>
        </div>
      </div>
      <div class="goodsInfo">
        <div class="triangle">
            <div><span>跟</span><span>踪</span><span>信</span><span>息</span></div>
        </div>
        <div class="content">
          <div class="content-left">
            <div class="box weight">
              <span class="title">货物重量</span>
              <span class="detial">1000</span>
              <span class="unit">千克</span>
            </div>
            <div class="box num">
              <span class="title">货物件数</span>
              <span class="detial">10</span>
              <span class="unit">件</span>
            </div>
            <div class="box size">
              <span class="title">货物体积</span>
              <span class="detial">0.50</span>
              <span class="unit">立方米</span>
            </div>
            <div class="box payWeight">
              <span class="title">计费重量</span>
              <span class="detial">1000.00</span>
              <span class="unit">千克</span>
            </div>
            <div class="box type">
              <span class="title">货物类型</span>
              <span class="detial">普货</span>
            </div>
            <div class="box name">
              <span class="title">货物名称</span>
              <span class="detial">服装</span>
            </div>
          </div>
          <div class="content-middle">
            <div class="box weight">
              <span class="title">实际重量</span>
              <span class="detial">1000.00</span>
              <span class="unit">千克</span>
            </div>
            <div class="box num">
              <span class="title">实际件数</span>
              <span class="detial">10</span>
              <span class="unit">件</span>
            </div>
            <div class="box size">
              <span class="title">实际体积</span>
              <span class="detial">0.50</span>
              <span class="unit">立方米</span>
            </div>
            <div class="box payWeight">
              <span class="title">实际计费重量</span>
              <span class="detial">1000.00</span>
              <span class="unit">千克</span>
            </div>
            <div class="box pack">
              <span class="title">货物包装</span>
              <span class="detial">纸箱</span>
            </div>
          </div>
          <div class="content-right">
            <div class="title">
              <p>货物尺寸</p>
              <p>(长*宽*高/件数)</p>
              <p>单位：cm</p>
            </div>
            <div class="val">
              <p>100*100*10/5</p>
              <p>100*100*10/5</p>
              <p>100*100*10/5</p>
              <p>100*100*10/5</p>
              <p>100*100*10/5</p>
              <p>100*100*10/5</p>
              <p>100*100*10/5</p>
              <p>100*100*10/5</p>
            </div>
          </div>
        </div>
      </div>
      <div class="fee-info">
        <div class="triangle">
            <div><span>费</span><span>用</span><span>信</span><span>息</span></div>
        </div>
        <div class="fee-top">
          <div class="box left">
            <h3>固定费用</h3>
            <div>
              <div class="key">航空运费</div>
              <div class="value">¥300.00</div>
            </div>
            <div>
              <div class="key">燃油附加费</div>
              <div class="value">¥120.00</div>
            </div>
            <div>
              <div class="key">出港处置费</div>
              <div class="value">¥10.00</div>
            </div>
            <div>
              <div class="key">出港制单费</div>
              <div class="value">¥100.00</div>
            </div>
            <div>
              <div class="key">进港提货费</div>
              <div class="value">¥100.00</div>
            </div>
            <div>
              <div class="key">上门提货费</div>
              <div class="value">¥10000.00</div>
            </div>
            <div>
              <div class="key">派送费</div>
              <div class="value">¥100.00</div>
            </div>
            <div class="total">
              <div class="key">合计</div>
              <div class="value">¥8800.00</div>
            </div>
          </div>
          <div class="box center">
            <h3>临时费用</h3>
          </div>
          <div class="box right">
            <h3>发票信息</h3>
            <div>
              <div class="key">企业名称：</div>
              <div class="value">深圳运捷讯息系统有限公司</div>
            </div>
            <div>
              <div class="key">纳税人识别号：</div>
              <div class="value">46546546464655465</div>
            </div>
            <div>
              <div class="key">注册地址：</div>
              <div class="value">深圳市福田区深南中路什么大厦1122</div>
            </div>
            <div>
              <div class="key">联系电话：</div>
              <div class="value">0755-156546465</div>
            </div>
            <div>
              <div class="key">开户行：</div>
              <div class="value">中国建设银行</div>
            </div>
            <div>
              <div class="key">开户行账号：</div>
              <div class="value">4135465416546464641654</div>
            </div>
            <div>
              <div class="key">开票人：</div>
              <div class="value">刘嬷嬷</div>
            </div>
            <div>
              <div class="key">开票人电话：</div>
              <div class="value">13546655454</div>
            </div>
            <div>
              <div class="key">开票人地址：</div>
              <div class="value">北京市朝阳区建国路</div>
            </div>

          </div>
        </div>
        <div class="fee-mid">
          <div class="had">
            <span class="title">已支付</span>
            <span class="value">¥8300.00</span>
          </div>
          <div class="need">
            <span class="title">待支付</span>
            <span class="value">¥0.00</span>
          </div>
        </div>
        <div class="fee-bot">
          <div class="box">
            <div>
              <div>
                <span class="key">系统交易流水号：</span>
                <span class="value">1354646464646854685468</span>
              </div>
              <div>
                <span class="key">交易时间：</span>
                <span class="value">2017-10-10 10:10:10</span>
              </div>
            </div>
            <div>
              <div>
                <span class="key">交易金额：</span>
                <span class="value">¥800</span>
              </div>
              <div>
                <span class="key">支付渠道：</span>
                <span class="value">新生支付</span>
              </div>
            </div>
          </div>
          <div class="box">
            <div>
              <div>
                <span class="key">系统交易流水号：</span>
                <span class="value">1354646464646854685468</span>
              </div>
              <div>
                <span class="key">交易时间：</span>
                <span class="value">2017-10-10 10:10:10</span>
              </div>
            </div>
            <div>
              <div>
                <span class="key">交易金额：</span>
                <span class="value">¥80</span>
              </div>
              <div>
                <span class="key">支付渠道：</span>
                <span class="value">支付宝</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  methods: {
    goto(path) {
      this.$router.push(path);
    }
  }
};
</script>
<style lang="scss" scoped>
.order_detail {
  // 左上角的三角
  .triangle {
    display: inline-block;
    position: absolute;
    left: 0;
    top: 0;
    width: 0;
    height: 0;
    border: 38px solid #fccf00;
    border-color: #fccf00 transparent transparent #fccf00;
    > div {
      display: inline-block;
      transform: rotate(-45deg) translate(-12px, -40px);
      color: #fff;
    }
  }
  .head {
    height: 61px;
    display: flex;
    .title {
      margin-left: 30px;
      line-height: 61px;
      display: grid;
      grid-template-columns: 1fr;
      // justify-items: center;
      align-items: center;
    }
  }
  .main {
    padding: 20px;
    .main-top {
      background-color: #fff;
      box-shadow: 3px 3px 3px #e0e0e0;
      .linear {
        height: 4px;
        background: linear-gradient(30deg, #fedb43 50%, #f52731 50%);
        background-size: 50px 4px;
      }
      .main-top-title {
        margin-top: 10px;
        display: flex;
        color: #a0a0a0;
        line-height: 20px;
        padding-left: 20px;
        .time {
          flex: 1;
        }
        .btn {
          width: 200px;
          text-align: right;
          .reset,
          .cancle {
            cursor: pointer;
            margin: 10px;
            &:hover {
              color: black;
            }
          }
        }
      }
      .content {
        padding: 0 20px;
        color: #a0a0a0;
        display: grid;
        grid-template-columns: 1fr 250px 250px;
        .left {
          .box {
            display: flex;
            margin: 10px 0;
            .title {
              font-weight: 700;
            }
            .detail {
              margin-left: 20px;
            }
          }
          .orderNum {
            .detail {
              color: #f42630;
              font-weight: 700;
              line-height: 20px;
            }
          }
          .baseserve,
          .moreserver,
          .increaseserver {
            .detail {
              display: flex;
              .item {
                margin: 0 20px;
                .get {
                  color: #8cc43f;
                  margin: 0 10px;
                }
                &.not {
                  .get {
                    color: #e6e6e6;
                  }
                }
              }
            }
          }
        }
        .middle {
          color: #fed001;
          width: 100%;
          text-align: center;
          padding-top: 30px;
        }
        .right {
          width: 100%;
          text-align: center;
          padding-top: 50px;
          button {
            padding: 4px 20px;
            box-shadow: 4px 4px 6px #e0e0e0;
          }
        }
      }
    }
    .server-info {
      position: relative;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      margin-top: 20px;
      background-color: #fff;
      box-shadow: 4px 4px 4px #e0e0e0;

      .box {
        height: 340px;
        border-right: 1px dashed #e0e0e0;
        border-bottom: 1px dashed #e0e0e0;
        &:nth-of-type(4n) {
          border-right: none;
        }
        &:nth-of-type(n + 5) {
          border-bottom: none;
        }
        .img {
          height: 44px;
        }
        .img,
        .title {
          text-align: center;
          margin: 20px 0;
          font-weight: 700;
        }
        .content {
          margin-top: 20px;
          color: #999;
          padding-left: 60px;
          .item {
            display: flex;

            span:first-child {
              width: 100px;
              text-align: justify;
              &::after {
                content: "";
                display: inline-block;
                width: 100%;
                overflow: hidden;
                height: 0;
              }
            }
            span:last-child {
              margin-left: 20px;
            }
          }
        }
      }
      .more {
        border-right: none;
        > div {
          width: 100%;
          // height: 100%;
          text-align: center;
          // margin-top: 50%;
          transform: translateY(150px);
        }
      }
    }
    .address {
      display: flex;
      height: 200px;
      margin-top: 20px;
      background-color: #fff;
      box-shadow: 4px 4px 4px #e0e0e0;
      position: relative;
      line-height: 20px;

      .center-icon {
        position: absolute;
        right: 50%;
        top: 50%;
        transform: translate(120%, -40%);
      }
      .left {
        // 中间的斜线
        &::before {
          position: absolute;
          content: "";
          right: 0;
          top: 0;
          width: 1px;
          height: 53%;
          background-color: #e6e6e6;
          transform-origin: 0px 0px;
          transform: rotate(-18deg);
        }
        &::after {
          position: absolute;
          content: "";
          right: 0;
          bottom: 0;
          width: 1px;
          height: 53%;
          background-color: #e6e6e6;
          transform-origin: center bottom;
          transform: rotate(18deg);
        }
        .icon {
          background-color: #ffda44;
        }
      }
      .right {
        .icon {
          background-color: #f4292f;
        }
      }
      .left,
      .right {
        flex: 1;
        padding-left: 80px;
        padding-top: 20px;
        position: relative;
        // 右下角icon
        .icon {
          width: 30px;
          height: 30px;
          border-radius: 50%;
          // background-color: #f4292f;
          position: absolute;
          bottom: 0;
          right: 0;
          text-align: center;
          line-height: 30px;
          color: #fff;
          margin: 0 10px 10px 0;
        }
        .box {
          display: flex;
          .key {
            width: 80px;
            text-align: justify;
            color: #999;
            &::after {
              content: "";
              display: inline-block;
              width: 100%;
              overflow: hidden;
              height: 0;
            }
          }
          .value {
            margin-left: 20px;
            color: #4d4d4d;
          }
        }
        .name-id,
        .phone-cellphone {
          .value {
            width: 150px;
          }
        }
      }
    }
    .goodsInfo {
      margin-top: 20px;
      box-shadow: 4px 4px 4px #e0e0e0;
      background-color: #fff;
      position: relative;
      .content {
        display: flex;
        .content-left,
        .content-middle {
          width: 300px;
          color: #9a9a9a;
          padding: 20px 0 20px 80px;
          border-right: 1px dashed #e0e0e0;
          .box {
            display: flex;
            margin: 10px 0;
          }
          .detial {
            width: 100px;
            color: #4e4e4e;
            text-align: center;
            font-weight: 700;
          }
          .unit {
            width: 80px;
            text-align: center;
          }
        }
        .content-middle {
          .box {
            .title {
              width: 100px;
              height: 20px;
              text-align: justify;
              &::after {
                content: "";
                display: inline-block;
                width: 100%;
                overflow: hidden;
                height: 0;
              }
            }
            .detial {
              color: #ffdb44;
            }
          }
          .pack {
            margin-top: 40px;
          }
        }
        .content-right {
          flex: 1;
          display: flex;
          .title {
            padding-top: 50px;
            width: 200px;
            vertical-align: middle;
            text-align: center;
            color: #989898;
          }
          .val {
            margin-top: 15px;
            width: 200px;
            height: 200px;
            border: 1px solid #989898;
            overflow: auto;
            padding: 0 0 0 10px;
          }
        }
      }
    }
    .fee-info {
      position: relative;
      margin-top: 20px;
      display: flex;
      flex-direction: column;
      background-color: #fff;
      box-shadow: 4px 4px 4px #e0e0e0;
      .fee-top {
        border: 1px dotted #e4e4e4;
        display: flex;
        padding-top: 20px;
        .box {
          line-height: 18px;
          > div {
            display: flex;
            .key {
              width: 100px;
              text-align: justify;
              margin-right: 20px;
              color: #989898;
              &::after {
                content: "";
                display: inline-block;
                width: 100%;
                overflow: hidden;
                height: 0;
              }
            }
            .value {
              color: #4d4d4d;
              font-weight: 700;
            }
          }
        }
        .left {
          flex: 2;
          padding-left: 60px;
          box-sizing: border-box;
          border-right: 1px dotted #e4e4e4;
          .total {
            margin-top: 30px;
          }
        }
        .center {
          flex: 2;
          border-right: 1px dotted #e4e4e4;
          padding-left: 20px;
        }
        .right {
          flex: 3;
          padding-left: 20px;
        }
      }
      .fee-mid {
        height: 100px;
        border-bottom: 8px dotted #e4e4e4;
        position: relative;
        text-align: right;
        .had {
          display: flex;
          margin-top: 20px;
          .title {
            flex: 1;
            font-size: 28px;
            color: #999999;
          }
          .value {
            width: 200px;
            font-size: 24px;
            text-align: left;
            margin-left: 20px;
            color: #fcd000;
            line-height: 37px;
          }
        }
        .need {
          display: flex;
          .title {
            flex: 1;
            font-size: 16px;
            color: #999999;
          }
          .value {
            width: 200px;
            text-align: left;
            margin-left: 20px;
            font-size: 16px;
            line-height: 21px;
            color: #999999;
          }
        }
        &::before {
          content: "";
          position: absolute;
          bottom: -19px;
          left: -15px;
          width: 30px;
          height: 30px;
          border-radius: 50%;
          background-color: #f7f7f7;
          box-shadow: -4px 0px 4px #e0e0e0 inset;
        }
        &::after {
          content: "";
          position: absolute;
          bottom: -19px;
          right: -15px;
          width: 30px;
          height: 30px;
          border-radius: 50%;
          background-color: #f7f7f7;
          box-shadow: 4px 0px 4px #e0e0e0 inset;
        }
      }
      .fee-bot {
        .box {
          display: flex;
          &:first-child {
            border-bottom: 1px dotted #e0e0e0;
          }
          > div {
            flex: 1;
            padding: 40px 0 20px 40px;
            > div {
              display: flex;
              .key {
                width: 150px;
                text-align: justify;
                color: #999999;
                &::after {
                  content: "";
                  display: inline-block;
                  width: 100%;
                  overflow: hidden;
                  height: 0;
                }
              }
              .value{
                color: #121212;
                font-weight: 700;
              }
            }
          }
        }
      }
    }
  }
}
</style>
