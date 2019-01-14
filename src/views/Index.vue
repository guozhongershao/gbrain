<template>
  <div class="index">
    <header class="top-title">
      <div class="sign">
        <a href="#">登陆</a> | <a href="#">注册</a>
      </div>
      <!-- router 跳转 -->
      <router-link to="/about"></router-link>
    </header>
    <div class="margint">
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Index',
    mounted() {
      window.addEventListener('scroll', this.handleScroll)
    },
    methods: {
      handleScroll() {
        let scrollTo = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop
        console.log(`ScrollTop : ${scrollTo}`)
      }
    }
  }
</script>

<style scoped>
  header {
    background: #e74c3c;
    color: white;
    height: 40px;
    width: 100%;
    position: fixed;
    top: 0;
    transition: top 1s;
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .hiddened {
    top: -90px;
  }

  .showed {
    top: 0;
    z-index: 9999;
  }

  .margint {
    z-index: 999;
    height: 2000px;
    background-color: antiquewhite;
  }

  .sign {
    position: absolute;
    left: 20%;
  }
</style>
