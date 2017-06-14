<template>
  <div class="hello">
    <h1 class="page-header">{{ msg }}</h1>
    <p> God said: {{ id }}</p>
    <div style="width:40%">
      <canvas id="myChart"></canvas>
    </div>
    
  </div>
</template>

<script>
export default {
  props: ['id'],
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App.'
    }
  },
  mounted () {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
