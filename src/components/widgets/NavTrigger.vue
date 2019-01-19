<!--
  nav 菜单trigger 按钮，
  提供用户自定义属性：
  size ; 按钮大小
  backgroundColor : 背景颜色
  tintColor : 按钮里横线的颜色
-->
<template>
  <button :style="customerStyle" class="nav-trigger" :class="{'nav-active' : isNavActive}" @click="toggleNavActive()">
    <span :style="{'background-color' : '#' + tintColor}"></span>
    <span :style="{'background-color' : '#' + tintColor}"></span>
    <span :style="{'background-color' : '#' + tintColor}"></span>
  </button>
</template>

<script>
  export default {
    name: "NavTrigger",
    data() {
      return {
        isNavActive: false,
        customerStyle: {
          // font-size 最小12px 原因未知，放大100倍，处理小于12px的尺寸
          'font-size': `${this.size * 100}px`,
          'background-color': `#${this.backgroundColor}`
        }
      }
    },
    props: {
      size: {
        default: 100, // 默认100px
      },
      backgroundColor: {
        default: 'ffffff',
        type: [String],
      },
      tintColor: {
        default: '000000'
      }
    },
    methods: {
      toggleNavActive() {
        console.log('active');
        if (this.isNavActive) {
          this.isNavActive = false;
        } else {
          this.isNavActive = true;
        }
      }
    }
  }
</script>

<style scoped>
  .nav-trigger {
    display: inline-block;
    width: 0.01em;
    height: 0.01em;
    margin: 0;
    border: 0;
    /* outline : none； 解决button有边框的问题 */
    outline: none;
    /* 解决背景颜色*/
    background-color: transparent;
    padding: 0 .00063em;
    transition: all .4s ease;
  }

  .nav-trigger span {
    display: block;
    width: 100%;
    height: 0.00126em;
    background-color: black;
    float: right;
    border-radius: 0.00095em;
    box-sizing: content-box;
    transition: all .3s ease;
    transform-origin: center center;
  }

  .nav-trigger span + span {
    margin-top: 0.00157em;
  }

  .nav-trigger span:last-child {
    width: 75%;
  }

  .nav-trigger:hover span, .nav-trigger.nav-active span {
    width: 100%;
  }

  .nav-trigger.nav-active {
    -webkit-transform: rotate(225deg);
    -ms-transform: rotate(225deg);
    transform: rotate(225deg);
  }

  .nav-trigger.nav-active span:first-child{
    -webkit-transform: rotate(90deg) translateX(0.00282em);
    -ms-transform: rotate(90deg) translateX(0.00282em);
    transform: rotate(90deg) translateX(0.00282em);
  }
  .nav-trigger.nav-active span:last-child{
    width: 100%;
    -webkit-transform: rotate(90deg) translateX(-0.00282em);
    -ms-transform: rotate(90deg) translateX(-0.00282em);
    transform: rotate(90deg) translateX(-0.00282em);
  }
</style>
