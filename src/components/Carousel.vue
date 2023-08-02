<template>
  <div 
    class="carousel-outline"
    @click="redirectLine"
  >
    <img src="../assets/photos/carousel1.png">
    <!-- <button class="line-btn"></button> -->
  </div>
</template>

<style lang="scss" scoped>
.carousel-outline{
  position: relative;
  padding: 10px 5px;
  width: 100%;
  // height: 50px;
  // border: 1px solid black;
  // background-color: #f8f4ee;
  img{
    width: 100%;
  }
}

</style>


<script>
export default {
  name: 'Carousel',

  methods:{
    redirectLine: function(){
      window.open('https://line.me/R/ti/p/@jh-gold');
    }
  }
}
</script>