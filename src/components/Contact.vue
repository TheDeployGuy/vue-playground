<template>
  <div class="contact">
    <p>Test value: {{ testValue }}</p>
  </div>
</template>

<script>
export default {
  props: ['testValue'],
  name: 'contact',
  data () {
    return {
      msg: 'Welcome to contact!'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
