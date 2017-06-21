<template>
  <div class="about">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'about',
  data () {
    return {
      msg: 'Welcome to about!'
    }
  },
  mounted () {
    console.log('Mounted')
    this.connectToSocket()
  },
  methods: {
    connectToSocket () {
      var websocket = new WebSocket('wss://echo.websocket.org')
      websocket.onopen = function () {
        websocket.send('SENT: Hello\n')
      }
      websocket.onmessage = function (s) {
        console.log('Rec ' + s.data)
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
