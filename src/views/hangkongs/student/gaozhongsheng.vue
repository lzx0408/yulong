<template>
  <div>
    <div class="lun_warp">
      <div class="lun_con">
        <img src="@/assets/img/高中生/高中生.png" alt="" />
      </div>
    </div>
    <div class="title_warp">
           
      <p>
                <router-link to="/" tag="span">当前位置：首页</router-link>
        <router-link to="/hangkong" tag="span">>航空学院</router-link>
               
        <router-link to="/chuzhongsheng">
          <span style="color: #999">>高中生</span>
        </router-link>
             
      </p>
         
    </div>
    <div class="major">
      <div class="mar-top">
        <img src="@/assets/img/高中生/当代高中生出路_03.jpg" alt="" />
      </div>
      <div class="mar-button">多岗位任你选择</div>
      <div class="mar-content">
        <div class="majors">
          <div class="maj-top">
            <img src="@/assets/img/公共/招生要求_24.jpg" alt="" />
          </div>
          <p>空乘专业</p>
        </div>
        <div class="majors">
          <div class="maj-top">
            <img src="@/assets/img/公共/招生要求_27.jpg" alt="" />
          </div>
          <p>高铁专业</p>
        </div>
        <div class="majors">
          <div class="maj-top">
            <img src="@/assets/img/公共/招生要求_30.jpg" alt="" />
          </div>
          <p>游轮海乘专业</p>
        </div>
        <div class="majors">
          <div class="maj-top">
            <img src="@/assets/img/公共/招生要求_31.jpg" alt="" />
          </div>
          <p>VIP地勤专业</p>
        </div>
      </div>
    </div>
    <!-- 未完成 -->
    <div class="kcdetail">
      <div class="mar-top">
        <img src="@/assets/img/高中生/未标题-2_03.jpg" alt="" />
      </div>
      <div class="en-content">
        <div class="content-bottom">
          <div>
            <img src="@/assets/img/高中生/高中生(1)_03.jpg" alt="" />
          </div>
          <div>
            <img src="@/assets/img/高中生/高中生(1)0_03.jpg" alt="" />
          </div>
        </div>
      </div>
      <div class="kc-text">
       可以在不同城市国家穿梭，除了可以练就空姐危机处理、耐心、温和、语言表达等能力及专业素质，还能接触各界人事，拓宽人脉。此外，空姐也是一个高薪职业，且受社会尊重和人们向往的一种群体，能够参与到空姐队伍中非常不错。
      </div>
      <div class="information_con_btm" @touchstart="seet()" @touchend="sett()">
        <img :src="setimg" alt="" />
      </div>
    </div>
   
    <div class="kczhiwei">
      <div class="ches-header">
        <img src="@/assets/img/高中生/空乘职位晋升详情_03.jpg" alt="" />
      </div>
      <div class="kczhiwei-img">
        <img src="@/assets/img/高中生/高中生晋升.png" alt="" />
      </div>
      <div class="kczhiwei-text">
        <div>一般学员在完成相应的业务培训后，可担当普通舱乘务员。</div>
        <div>
          随着飞行小时数的增加，个人资历的提升，通过相应的考核，可提升为两舱/头等舱乘务员。
        </div>
        <div>
          头等舱乘务员考核期满后，可担当区域乘务长，成绩优秀的区域乘务长经过考评委员会严格的考评后，可担当主任乘务长，并可以独立带班执行国际航班以及首长专机任务。
        </div>
        <div>
          负责做好本部门岗位分工，规范各岗位工作规定和规程，负责客舱服务部人事考核等人力资源工作，主持分析本部门的工作进度。
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      setimg: require("@/assets/img/公共/航空专业详情页_04.jpg"),
    };
  },
  methods: {
    seet() {
      this.setimg = '';
    },
    sett() {
      this.setimg = '';
    },
  },
};
</script>

<style lang='scss' scoped>
.title_warp {
  width: 100%;
  padding: 0 0.2rem;
  margin: 0.15rem 0;
  box-sizing: border-box;
    p {
    width: 3.75rem;
    margin: 0 auto;
        span {
      margin-left: 0.2rem;
      font-size: 0.14rem;
      font-weight: normal;
      font-stretch: normal;
      line-height: 0.07rem;
      letter-spacing: 0px;
      color: #888888;
    }
        .hang {
      margin-left: 0.05rem;
      font-family: PingFang-SC-Medium;
      font-size: 0.14rem;
      font-weight: normal;
      letter-spacing: 0px;
      color: #b0b0b0;
    }
  }
}
.lun_warp {
  width: 100%;
  height: 1.5rem;
  .lun_con {
    width: 3.75rem;
    height: 1.5rem;
    margin: 0 auto;
    img {
      width: 100%;
      height: 100%;
    }
  }
}
.major {
  width: 3.55rem;
  margin: 0.15rem auto;
  background: #fff;
  border-radius: 0.05rem;
  // overflow: hidden;
  .mar-top {
    width: 100%;
    height: 0.55rem;
    img {
      width: 100%;
      height: 100%;
    }
  }
  .mar-button {
    width: 1.4rem;
    height: 0.35rem;
    margin: 0.15rem auto 0;
    background-color: #3abbc9;
    border-radius: 0.17rem;
    text-align: center;
    line-height: 0.35rem;
    font-size: 0.17rem;
    color: #fff;
  }
  .mar-content {
    width: 100%;
    padding-bottom: 0.1rem;
    font-size: 0.14rem;
    text-align: center;
    overflow: hidden;
    .majors {
      width: 1.63rem;
      margin: 0.1rem 0 0 0.1rem;
      float: left;
      .maj-top {
        width: 100%;
        height: 1.34rem;
        margin-bottom: 0.1rem;
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
}

.kcdetail {
  width: 3.55rem;
  margin: 0.15rem auto;
  background: #fff;
  border-radius: 0.05rem;
  padding-bottom: .01rem;
  .mar-top {
    width: 100%;
    height: 0.55rem;
    img {
      width: 100%;
      height: 100%;
    }
  }
  .en-content {
    width: 100%;
    padding: 0.1rem 0.1rem;
    box-sizing: border-box;
    .content-bottom {
      width: 100%;
      padding-top: 0.1rem;
      display: flex;
      justify-content: space-between;
      div {
        width: 1.63rem;
        height: 1.63rem;
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
  .kc-text {
    width: 3.3rem;
    height: 1rem;
    // box-sizing: border-box;
    border-radius: 0.15rem;
    border: solid 0.01rem #999999;
    margin: 0 auto;
    font-size: 0.12rem;
    padding: 0 0.1rem;
    text-indent: 0.12rem;
    line-height: 0.23rem;
    // font-weight: 900;
    // letter-spacing: 0px;
  }
  .information_con_btm {
          margin: .18rem;
          text-align: center;
          img {
            width: .24rem;
            
          }
  }
}
.ches {
  width: 3.55rem;
  margin: auto;
  background: #fff;
  overflow: hidden;
  border-radius: 0.05rem;
  margin-top: 0.1rem;
  margin-bottom: 0.1rem;
  .ches-header {
    width: 100%;
    img {
      width: 100%;
    }
  }
  .ches-text {
    padding: 0.11rem 0.05rem 0.16rem 0.06rem;
    box-sizing: border-box;
    ul {
      li {
        display: flex;
        justify-content: space-between;
        .text-img {
          width: 50%;
          height: 1.4rem;
          img {
            width: 100%;
            height: 100%;
          }
        }
        .text-text {
          width: 50%;
          padding: 0.18rem 0 0 0.18rem;
          box-sizing: border-box;
          .text-header {
            display: flex;
            .text-header-img {
              width: 0.27rem;
              height: 0.3rem;
              float: left;
              img {
                width: 100%;
                height: 100%;
              }
            }
            .text-header-text {
              height: 0.3rem;
            }
            p {
              line-height: 0.3rem;
              padding-left: 0.1rem;
              font-size: 0.14rem;
            }
          }
          .text-header-text {
            font-size: 0.12rem;
          }
        }
      }
    }
  }
}
.kczhiwei {
  width: 3.55rem;
  margin: 0 auto 0.15rem;
  padding: 0 0 0.15rem 0;
  background: #fff;
  .ches-header {
    width: 100%;
    img {
      width: 100%;
    }
  }
  .kczhiwei-img {
    width: 3.35rem;
    height: 1.4rem;
    padding: 0.1rem 0.1rem;
    img {
      width: 100%;
      height: 100%;
    }
  }
  .kczhiwei-text {
    width: 100%;
    background: url("~@/assets/img/高中生/高中生_03.jpg") no-repeat;
    background-size: 90% 100%;
    margin: 0.1rem 0 0 0;
    font-size: 0.12rem;
    div {
      padding: 0.13rem 0.2rem 0 1.4rem;
      // line-height: .18rem;
      // font-weight: 900;
    }
  }
}
</style>
