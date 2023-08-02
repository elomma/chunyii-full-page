<template>
  <div class="service-outline">
    <div v-for="service in serviceList" class="service-col">
      <img :src="service.serviceImg" />
      <h5 class="service-text">{{ service.serviceText }}</h5>
    </div>
  </div>
</template>

<script>
import serviceImg1 from "@/assets/photos/service1.jpg";
import serviceImg2 from "@/assets/photos/service2.jpg";
import serviceImg3 from "@/assets/photos/service3.jpg";
import serviceImg4 from "@/assets/photos/service4.jpg";
import serviceImg5 from "@/assets/photos/service5.jpg";

export default {
  name: "serviceOutlive",

  data() {
    return {
      serviceList: [
        { serviceText: "財富管理", serviceImg: serviceImg1 },
        { serviceText: "存股通", serviceImg: serviceImg2 },
        { serviceText: "一戶通", serviceImg: serviceImg3 },
        { serviceText: "便利貸", serviceImg: serviceImg4 },
        { serviceText: "借券專區", serviceImg: serviceImg5 },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.service-outline {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 35px 10px;
  // height: 100px;
  // border: 1px solid red;
}

.service-col {
  position: relative;
  width: 20%;
  height: 60px;
  // border: 1px solid red;
  img {
    position: absolute;
    width: 100%;
    height: 100%;
  }
}

.service-text {
  position: absolute;
  color: #444;
  font-size: 0.75rem;
  left: 10px;
  z-index: 100;
}

@media screen and (max-width: 650px) {
}
</style>
