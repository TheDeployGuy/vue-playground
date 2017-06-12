<template>
<ul class="nav nav-sidebar">
  <li><router-link to="/">Home</router-link></li>
  <li><router-link to="/about">About</router-link></li>
  <li><router-link to="/contact">Contact</router-link></li>
</ul>
</template>

<script>
export default {
  name: 'navbar',
  data () {
    return {
      msg: 'Welcome to navbar'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .nav-sidebar > li > a {
    font-size: 20px !important;
  }

    /* Sidebar navigation */
  .nav-sidebar {
    margin-right: -21px; /* 20px padding + 1px border */
    margin-bottom: 20px;
    margin-left: -20px;
  }
  .nav-sidebar > li > a {
    padding-right: 20px;
    padding-left: 20px;
  }
  .nav-sidebar > .active > a,
  .nav-sidebar > .active > a:hover,
  .nav-sidebar > .active > a:focus {
    color: #fff;
    background-color: #428bca;
  }
</style>
