<template>
    <div class="header">
      <div class="logo">
        <img src="../assets/photos/logo.png" alt="">
      </div>
      <div class="header-right">
        <div class="login-btn">
          登入
        </div>
        <div class="search-icon">
          <img src="../assets/photos/search.png">
        </div>
        <div class="hamburger">
          <div class="burger-outline">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>


.header{
  display: flex;
  padding: 1px;
  width: 100vw;
  box-sizing: border-box;

  .logo{
    width: 65%;
    display: flex;

    img{
      width: 35%;
    }
  }

}

.header-right{

  width: 35%;
  display: flex;
  align-items: center;
  justify-content: center;

  div{
    flex:1;
    text-align: center;
  }


  .login-btn{
    background-color: transparent;
    border: 1px solid #BE9835;
    color: #be9835;
    padding: 3px;
    font-size: 12px;
    border-radius: 200px;
    font-weight: bold;
}
  .search-icon{
    text-align: center;
    img{
      width: 35%;
    }
  }

  .hamburger{
    text-align: center;
    .burger-outline{
      width: 30px;
      height: 30px;
      // border: 1px solid red;

      text-align: center;
      display: flex;
      flex-direction:column;
      justify-content: center;

      span{
        height: 4px;
        background-color: #d42b45;
        margin: 3px 0;
        border-radius: 5px;
      }
    }
  }

  
}


@media screen and (max-width: 700px) {
  .header{


  .logo{


    img{
      width: 75%;
    }
  }

}

}


</style>


<!-- <script>
export default {
  data() {
    return {
      
    };
  },
  methods: {
  
  },
  computed: {
  
  },
  mounted() {
  
  }
};
</script> -->