<template>
  <div class="about">
    <h1>{{ msg }}</h1>
    <div v-if="posts.length > 0">
       <contact :testValue="posts"></contact>
    </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Contact from '@/components/Contact'
export default {
  name: 'about',
  components: {
    Contact
  },
  data () {
    return {
      msg: 'Welcome to about!',
      posts: []
    }
  },
  beforeMount () {
    axios.get('http://jsonplaceholder.typicode.com/posts')
      .then(response => {
        this.posts = response.data
      })
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
