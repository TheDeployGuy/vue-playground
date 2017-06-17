<template>
<div>
  <Navbar></Navbar>
  <Sidebar></Sidebar>
  <div style="margin-left:25%; width:80%;">
    <router-view></router-view>
  </div>
</div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Sidebar from '@/components/Sidebar'
export default {
  name: 'dashboard',
  components: {
    Navbar, Sidebar
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
 
}
</style>
