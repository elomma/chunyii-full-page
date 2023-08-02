<template>
  <div class="main-page">
    <!-- left -->
    <div class="main-content main-left">
      <h3>最新消息</h3>
      <div class="switch-col">
        <div class="switch-title" v-for="title in leftSwitch">
          {{ title }}
        </div>
      </div>
      <hr />
      <ul class="content-list">
        <li v-for="text in leftCol">
          {{ text.title }}{{ text.text }}
          <hr />
        </li>
      </ul>
    </div>
    <!-- mid -->
    <div class="main-content main-mid">
      <h3>國際市場行情</h3>
      <div class="switch-col">
        <div class="switch-title" v-for="title in midSwitch">
          {{ title }}
        </div>
      </div>
      <div class="stock-top">
        <div v-for="stockInfo in stockTitle" class="stock-title">
          {{ stockInfo }}
        </div>
      </div>
      <!--  -->
      <div v-for="stockInfo in midCol" class="stock-info-wrap">
        <span class="stockInfo-text stockInfo-text1"> {{ stockInfo.stockName }}</span>
        <span class="stockInfo-text stockInfo-text2">{{ stockInfo.stockData}}</span>
        <span 
          class="stockInfo-text stockInfo-text3"
          :class="{ toRed: checkResult(stockInfo.result), toGreen:!checkResult(stockInfo.result)}"
        >
          {{ stockInfo.result }}
        </span>
        <hr>
      </div>

    </div>
    <!-- right -->
    <div class="main-content main-right">
      <h3>今日大盤</h3>
      <div class="switch-col">
        <div class="switch-title" v-for="title in leftSwitch">
          {{ title }}
        </div>
      </div>
      <div class="stock-photo">
        <img src="../assets/photos/stockPhoto.jpg" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainPge",

  data() {
    return {
      leftCol: [
        {
          title: "【嚴防詐騙】",
          text: "為保障您的帳戶交易及個資安全，請留意詐騙集團恐偽冒營業員或業務主管誘使您提供個資，請勿隨意告知他人帳號、密碼等個人資訊!",
        },
        {
          title: "【嚴防詐騙】",
          text: "請認明群益金鼎證券官方網址，請勿下載來源不明APP",
        },
        {
          title: "【求償公告】 ",
          text: "即日起至112年7月18日受理飛寶公司財報不實案，投資人求償登記事宜。",
        },
        {
          title: "【公告訊息】",
          text: "2023年7月份複委託海外股市休市日，提醒投資人注意各市場之開休異動。",
        },
        {
          title: " ",
          text: "集保股利發放電子通知服務上線，同意接收電子通知，千萬獎金集保送",
        },
        {
          title: "【股神交易爭霸賽】",
          text: "【股神交易爭霸賽】人類程式、雙戰線，等你來戰！",
        },
      ],
      midCol:[
        {stockName:'恒生香港綜合指數', stockData: 2961.41, result: '+41.36'},
        {stockName:'國企指數現貨', stockData: 6670.68, result: '+121.49'},
        {stockName:'深圳綜合指數', stockData: 2027.73, result: '-9.74'},
        {stockName:'韓國漢城指數', stockData: 2063.81, result: '+11.45'},
        {stockName:'恒生指數現貨', stockData: 16939, result: '+273.91'},
        {stockName:'英國時報金融指數', stockData: 7697, result: '+21'},
      ],

      leftSwitch: ["訊息公告", "即時新聞"],
      midSwitch: ["國際股市", "期指行情"],
      rightSwitch: ["今日大盤", "櫃買中心"],

      stockTitle: ["市場類別", "指數", "漲跌"],
    };
  },
  methods:{

    checkResult(resultData){

      let result = resultData.slice(0,1);

      if(result == '+'){
        return true
      }
      return false;

    },
  },

  created(){

    
  }

};
</script>

<style lang="scss" scoped>

.toRed{
  color:red;
}

.toGreen{
  color: rgb(23, 182, 23)
}

h3 {
  margin: 3px 0;
  font-family: Noto Sans TC, sans-serif, 微軟正黑體, Microsoft JhengHei, Roboto,
    Arial, Helvetica;
  color: #444;
  font-size: 20px;
}

.content-list {
  list-style: none;
  margin: 0;
  padding: 0;

  li {
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    padding: 5px 0;
    font-size: 0.85rem;
  }
}

hr {
  margin: 0;
}


.main-page {
  display: flex;

  width: 100%;
  height: 250px;
  padding: 0 8px;

  .main-content {
    padding: 0 3px;
    width: 33%;
    // border: 2px solid orange;
  }
}

.switch-col {
  display: flex;
  :first-child {
    background-color: #ee8897 !important;
    // border: 1px solid #d42b45 !important;
    color: white !important;
    font-weight: bold;
  }

  .switch-title {
    width: 120px;
    height: 35px;
    background-color: #f5f5f5;
    border: 1px solid #dcdcdc;
    color: rgb(177, 177, 177);
    font-weight: bold;

    display: flex;
    justify-content: center;
    align-items: center;
  }
}

.stock-top {
  display: flex;

  .stock-title {
    flex: 1;
    font-family: "微軟正黑體", Microsoft JhengHei, Roboto, Arial, Helvetica;
    color: #84754e;
    font-weight: bold;
    font-size: 0.95rem;
    padding: 5px 0;
  }
}

.stockInfo-text{
  display: inline-block;
  padding: 3px 0;
}
.stockInfo-text1{
    width: 45%;
    color: #444;
    font-weight: bold;
    font-family: Noto Sans TC,sans-serif,微軟正黑體,Microsoft JhengHei,Roboto,Arial,Helvetica;
    font-size: .85rem;
  }
  .stockInfo-text2{
    width: 30%;
    font-size: .95rem;
    font-family:'微軟正黑體';
    font-weight: bold;
  }
  .stockInfo-text3{
    width: 25%;
    font-size: .85rem;
    font-weight: bold;
    font-family:'微軟正黑體'
  }

.stock-photo{
  img{
    width: 100%;
    height: 200px;
  }
}

@media screen and (max-width: 650px) {

  .main-page {
    display: inline-block;

    width: 100%;
    height: 250px;
    padding: 0 8px;

    .main-content {
      padding: 0 3px;
      width: 100%;
      // border: 2px solid orange;
    }
  }

.stock-photo{
    img{

      width: 70%;
      // height: 150px;
    }
}
  
}
</style>
