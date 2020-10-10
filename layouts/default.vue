<template>
  <div class="content">
    <top-bar></top-bar>
    <Nuxt />
    <bottom-bar></bottom-bar>
  </div>
</template>

<script>
import TopBar from '@/components/layouts/TopBar.vue'
import BottomBar from '@/components/layouts/BottomBar.vue'
export default {
  components:{
    TopBar,
    BottomBar
  }
}
</script>
<style scoped>
html,body{
  width: 100%;
  min-width: 1300px;
}
html,body,div{
  margin: 0;
  padding: 0;
}
a{
  text-decoration: none;
  color: black;
  cursor: pointer;
}
ul,li{
  padding: 0;
  margin: 0;
  list-style: none;
}


</style>
