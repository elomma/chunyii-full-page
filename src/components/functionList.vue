<template>
  <div class="function-outline">
    <div class="function-list">
      <div v-for="functionData in functionsIconList" class="icon-Wrapper">
        <div class="icon-img">
          <img :src="functionData.iconSrc" alt="" />
        </div>
        <div class="icon-text">{{ functionData.iconText }}</div>
      </div>
    </div>
  </div>
</template>

<script>
import function1 from "@/assets/photos/icon15.svg";
import function2 from "@/assets/photos/icon15.svg";
import function3 from "../assets/photos/icon16.svg";
import function4 from "../assets/photos/icon17.svg";
import function5 from "../assets/photos/icon18.svg";
import function6 from "../assets/photos/icon19.svg";
import function7 from "../assets/photos/icon20.svg";

export default {
  name: "functionList",

  data() {
    return {
      functionsIconList: [
        {
          iconText: "證券資料",
          iconSrc: function1,
        },
        {
          iconText: "期貨資料",
          iconSrc: function2,
        },
        {
          iconText: "線上開戶",
          iconSrc: function3,
        },
        {
          iconText: "密碼專區",
          iconSrc: function4,
        },
        {
          iconText: "憑證專區",
          iconSrc: function5,
        },
        {
          iconText: "線上簽署",
          iconSrc: function6,
        },
        // {
        //   iconText: "帳單查詢",
        //   iconSrc: function7,
        // },
      ],
    };
  },

  // created: function () {
  //   console.log("imgIcon", imgIcon);
  // },
};
</script>

<style lang="scss" scoped>
.function-outline {
  padding: 10px 10px;
  width: 100%;
  background-color: #e7e7e7;
}

.function-list {
  display: flex;
  justify-content: center;
  align-items: center;
  // height: 350px;
  flex-wrap: wrap;
}

.icon-Wrapper {
  display: flex;
  flex-direction: column;
  // height: 100px;
  flex: 1;
  min-width: 55px;
  max-width: 100px;
  // height: 100%;
}

.icon-img {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 70%;
  // width: 100%;
}

.icon-text {
  text-align: center;
  // width: 100%;
  height: 30%;
  font-size: 0.95rem;
  color: #444;
  font-family: Noto Sans TC, sans-serif, 微軟正黑體, Microsoft JhengHei, Roboto;
  font-weight: bold;
}

@media screen and (max-width: 700px) {
  .icon-text {
    font-size: 0.75rem;
  }

  .icon-img {
    img {
      width: 70%;
    }
  }
}
</style>
