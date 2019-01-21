<template>
  <div class="cube-canvas" :class="{'cube-canvas-hide': isCubeHide}">
    <div class="cube-container">
      <img src="../../assets/cube.gif" alt="preload spinner">
      <div class="cube-title">
        <h4>G-BRAIN</h4>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "CubeMask",
    data(){
      return {
        isCubeHide : false,
      }
    },
    mounted() {
      setTimeout(()=>{
        this.isCubeHide = true;
      }, 2000);
    }
  }
</script>

<style scoped>
  .cube-canvas-hide{
    opacity: 0;
    transition: opacity 0.5s;
  }

  .cube-canvas {
    background: #fff;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    top: 0;
  }

  .cube-container img {
    margin-left: 38px;
  }

  .cube-container,
  .cube-title {
    height: 200px;
    left: 50%;
    margin: -100px 0 0 -100px;
    position: absolute;
    top: 50%;
    width: 200px;
  }

  .cube-title {
    left: 0;
    margin: 0;
    text-align: center;
    top: 65%;
  }

  .cube-title h4 {
    color: #555;
    text-transform: uppercase;
    margin-top: 15px;
    font-size: 2em;
  }
</style>
