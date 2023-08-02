<template>
  <div class="footer-out-wrap">
    <div class="footer-main">
      <div v-for="msg in footerTitle" class="main-msg">
       {{ msg }}
      </div>
    </div>
    <hr>

    <!-- about -->
    <div class="footer-sub">
      <div v-for="msg in footerSubTitle" class="sub-msg">
       {{ msg }}
      </div>
    </div>

    
  </div>
</template>

<script>
export default {
  name: "footerPage",

  data() {
    return {
      footerTitle:[
        '群益期貨', '群益投顧','群益保險', 
        '群益投信', '群益香港', '群益上海'
      ],
      footerSubTitle:[
        '關於群益 | ','網站聲明 | ','人才招募 | ',
        '金融友善服務專區 | ','永續發展專區 | ','防制金融詐騙專區 | ',
        '洗錢防制 | ','電子化金融服務專區 | ','營業據點 | ','金融學苑 | ','影音網 | ',
      ],
      footerTel:'語音下單專線：4050-3688 | 客服服務專線：412-8878 (手機請加02，國外地區客戶請撥：886-2-412-8878) | 服務時間：8：00-17：00(股市交易日)',
      footerBzName:'營業人名稱：群益金鼎證券股份有限公司統一編號：22956035',
      footerCopyRight: '© 群益金融集團 版權所有© 2023Capital Group All Rights Reserved'
    }

  }
}

</script>

<style lang="scss" scoped>

hr{
  background-color: black;
}
.footer-out-wrap{
  background-color: #f7e9c8;
  margin-top: 80px;
  padding: 30px 0;
}
.footer-main{
  display: flex;
  justify-content: center;
  text-align: center;
  // margin-top: 80px;
  // padding: 50px 0;
  // background-color: #f7e9c8;
  flex-wrap: wrap;
}

.main-msg{
  padding: 0 8px;
  color: #84754e;
  font-weight: bold;
  font-size: 18px;

  font-family: '微軟正黑體'
}

.footer-sub{
  padding: 5px 0;
  display: flex;
  justify-content: center;
  text-align: center;
  flex-wrap: wrap;
  color: #444;
}

.sub-msg{
  font-size: 10px;
  font-weight: bold;
  padding: 0 3px;
}

</style>