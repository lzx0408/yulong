<template>
  <div class="information_warp">
    <div class="information_con">
      <div class="information_con_top">
        <img src="@/assets/img/公共/首页改1_91.gif" alt="" />
      </div>
      <div class="information_con_cen">
        <ul class="btm_list">
          <li v-for="(item,index) in listWen" :key="index.article_clicknum" @click="Xiangqing(index)">
            <router-link  :to="{path:'/message',query:{cid:item.article_id}}">
            
              <img
                style="width: 0.16rem; padding-bottom: 0.02rem"
                src="@/assets/img/shouye/首页_03.jpg"
                alt=""
              />
              {{item.article_name}}
            </router-link>
            <p>{{formatTime(item.article_atime)}}</p>
          </li>
         
        </ul>
      </div>
      <div class="information_con_btm" @touchstart="seet()" @touchend="sett()">
        <img :src="setimg" alt="" />
      </div>
    </div>
  </div>
</template>
<script>
import moment from 'moment'
import axios from "axios"
export default {
  data() {
    return {
      setimg: require("@/assets/img/公共/航空专业详情页_04.jpg"),
      listWen:[],
      url: "http://39.105.137.169:9527/",
    };
  },
   mounted(){
    axios.get("/cw", { params: { mod: "news" } }).then((res)=>{
      console.log(res);
      this.listWen = res.data.wen;
    })
  },
  methods: {
    Xiangqing(index){
      // console.log(this.listText[index].article_text)
      this.$store.commit('Xiangqing',this.listWen[index].article_text)
    },
    seet() {
      this.setimg = "";
    },
    sett() {
      this.setimg = "";
    },
    formatTime(value) {
      const time = "YYYY.MM.DD";
      return moment(value * 1000).format(time);
    },
  },
};
</script>

<style lang="scss" scoped>
.information_warp {
  width: 100%;
  height: auto;
  min-width: 3.56rem;
  background: #eaeaea;
  margin-top: .15rem;
  .information_con {
    width: 3.55rem;
    height: 100%;
    margin: 0 auto;
    background: #ffffff;
    border-radius: 0.05rem;
    padding-bottom: .01rem;
    .information_con_top {
      width: 100%;
      height: 0.55rem;
      img {
        width: 100%;
        height: 100%;
      }
    }
    .information_con_cen {
      width: 100%;
      height: 100%;
      .btm_list {
        width: 3.56rem;
        height: 100%;
        li {
          padding: 0.2rem 0.05rem 0 0.07rem;
          border-bottom: 1px solid #ccc;
          overflow: hidden;
          a {
            float: left;
            font-family: PingFang-SC-Medium;
            font-size: 0.15rem;
            font-weight: normal;
            font-stretch: normal;
            letter-spacing: 0px;
            color: #333333;
            width: 2.41rem;
            display: -webkit-box;
            -webkit-box-orient: vertical;
            -webkit-line-clamp: 1;
            overflow: hidden;
          }
          p {
            float: right;
            font-family: PingFang-SC-Medium;
            font-size: 0.14rem;
            font-weight: normal;
            font-stretch: normal;
            letter-spacing: 0px;
            color: #999999;
            margin-bottom: 0;
          }
        }
      }
    }
    .information_con_btm {
      margin: .18rem;
      text-align: center;
      img {
        // width: 3.31rem;
        width: 0.24rem;
        // margin: auto;
      }
    }
  }
}
</style>