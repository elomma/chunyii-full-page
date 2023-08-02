<template>
  <div id="app">

    <!-- serviceIcon-->
    <img 
      class="service-icon"
      src="./assets/photos/serviceIcon.png"
      @click="redirectLine"
    >
    <HeaderCol />
    <Carousel />
    <functionsCol />
    <ServiceCol />
    <MainCol />
    <FooterPage />

    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view/> -->
  </div>
</template>

<script>
import HeaderCol from "./components/HeaderCol.vue";
import Carousel from "./components/Carousel";
import functionsCol from "./components/functionList";
import ServiceCol from "./components/ServiceCol";
import MainCol from "./components/MainCol";
import FooterPage from "./components/FooterPage";



window.onload=function(){
  imgDom= document.querySelector(".service-icon");
}


let imgDom;

let moveIcon = function(){
    // 卷軸高度
    let scroll = window.scrollY;
    // 新高度
    let newDis = scroll+250+'px'
    imgDom.style.top = newDis
}

window.addEventListener("scroll", moveIcon);


export default {
  components: {
    HeaderCol,
    Carousel,
    functionsCol,
    ServiceCol,
    MainCol,
    FooterPage
  },

  data(){
    return{
      imgDom: document.querySelector(".service-icon"),
    }
  },

  methods:{
    redirectLine: function(){
      window.open('https://line.me/R/ti/p/@jh-gold');
    }
  },

  created(){
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
html,
body {
  width: 100%;
  margin: 0;
  padding: 0;
  /* overflow-y: scroll;
  overflow-x: hidden; */
}

.service-icon{
  position: absolute;
  width: 50px;
  right: 20px;
  top: 250px;
  z-index: 99;
  border-radius: 200px;
  
  cursor: pointer;
}
</style>
