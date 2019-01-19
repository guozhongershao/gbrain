<template>
  <div class="index">
    <header :class="{hiddened : scrollDown, showed : scrollUp}">
      <div class="sign">
        <span class="iconfont icon-Account" style="position: relative; top: 0.1em;">&nbsp;</span><a href="#">登陆</a> | <a href="#">注册</a>
      </div>
      <!-- router 跳转 -->
      <!--<router-link to="/about"></router-link>-->
    </header>
    <main class="margint">

    </main>
    <footer>
      <div style="width: 100%; text-align: center; background-color: #cccccc; color: #969896">Copyright</div>
    </footer>
  </div>
</template>

<script>
  export default {
    name: 'Index',
    data(){
      return {
        // 控制头部的显示
        lastScrollY: 0,
        scrollUp : false,
        scrollDown : false,
      }
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll)
    },
    computed :{
    },
    watch: {
      lastScrollY (newOffset, oldOffset) {
        console.log(`newOffset : ${newOffset}`);
        console.log(`oldOffset : ${oldOffset}`);
        if (newOffset > oldOffset){ // 向下滚
          this.scrollDown = true;
          this.scrollUp = false;
        }else if(newOffset < oldOffset){ // 向上滚
          this.scrollUp = true;
          this.scrollDown = false;
        }
      },
    },
    methods: {
      handleScroll() {
        this.lastScrollY = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
        console.log(`ScrollTop : ${scrollTo}`);
      },
    },
  }
</script>

<style scoped>
  header {
    background: #336699;
    color: white;
    height: 40px;
    width: 100%;
    position: fixed;
    transition: top 1s;
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
  }

  .hiddened {
    top: -90px;
    z-index: 9999;
  }

  .showed {
    top: 0;
    z-index: 9999;
  }

  .margint {
    width: 100%;
    height: 2000px;
    padding-top: 40px;
    background-color: white;
  }

  .sign {
    text-align: center;
    margin-right: 50px;
  }
</style>
