<template>
  <nav-trigger :size=32 tint-color="336699" @click.native="clis()"></nav-trigger>
</template>

<script>
  import NavTrigger from '../components/widgets/NavTrigger.vue'

  export default {
    name: "Index",
    components: {
      NavTrigger,
    },
    methods: {
      clis(){
        console.log('test');
      }
    }
  }
</script>

<style scoped>

</style>
