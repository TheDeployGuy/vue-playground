<template>
 <nav>
    <div class="nav-wrapper">
      <a href="#!" class="brand-logo center">Vue Playground</a>
      <a href="#" data-activates="mobile-demo" class="button-collapse"><i class="material-icons">menu</i></a>
      <ul class="right hide-on-med-and-down">
        <li><a href="!#">Sign up</a></li>
        <li><a href="!#">Login</a></li>
      </ul>
      <ul class="side-nav" id="mobile-demo">
        <li><a href="!#">Sign up</a></li>
        <li><a href="!#">Login</a></li>
      </ul>
    </div>
  </nav>
         
</template>

<script>
import $ from 'jquery'
export default {
  name: 'navbar',
  data () {
    return {
      msg: 'Welcome to navbar'
    }
  },
  mounted () {
    $('.button-collapse').sideNav()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
