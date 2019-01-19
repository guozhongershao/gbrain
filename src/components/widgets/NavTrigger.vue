<template>
  <button class="nav-trigger" :class="{'nav-active' : isNavActive}" @click="toggleNavActive()">
    <span></span>
    <span></span>
    <span></span>
  </button>
</template>

<script>
  export default {
    name: "NavTrigger",
    data() {
      return {
        baseSize: 10, // 默认大小 10px
        isNavActive: false,
      }
    },
    props: {
      size: {
        default: 10,
      }
    },
    methods: {
      toggleNavActive(){
        console.log('active');
        if (this.isNavActive){
          this.isNavActive = false;
        }else{
          this.isNavActive = true;
        }
      }
    }
  }
</script>

<style scoped>
  .nav-trigger {
    display: inline-block;
    width: 3.5rem;
    height: 2.9rem;
    padding: 0;
    margin: 0;
    border: 0;
    background-color: transparent;
    padding: 0 .2rem;
  }

  .nav-trigger span {
    display: block;
    width: 100%;
    height: 0.4rem;
    background-color: black;
    float: right;
    transition: all 0.4s ease;
    border-radius: 0.3rem;
    box-sizing: content-box;
  }

  .nav-trigger span + span {
    margin-top: 5px;
  }

  .nav-trigger span:last-child {
    width: 75%;
  }

  .nav-trigger:hover span, .nav-trigger:active span {
    width: 100%;
  }

  .nav-trigger .is
</style>
