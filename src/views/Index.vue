<template>
  <div class="index-background">
    <nav-trigger :size=32 tint-color="ffffff" @click.native=""></nav-trigger>
    <cube-mask></cube-mask>
  </div>
</template>

<script>
  import NavTrigger from '../components/widgets/NavTrigger.vue'
  import CubeMask from '../components/widgets/CubeMask.vue'

  export default {
    name: "Index",
    components: {
      NavTrigger,
      CubeMask,
    },
    methods: {
    }
  }
</script>

<style scoped>
  .index-background {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: url("../assets/bg1280x788.jpg") no-repeat;
    background-size: 100%;
  }
</style>
