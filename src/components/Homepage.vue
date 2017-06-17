<template>
  <div class="homepage">
    <p> God said: {{ id }}</p>
    <div style="width:40%">
      <Chart :chartData="datacollection"></Chart>
    </div>

    
      <canvas id="myChart"></canvas>
    
    </div>
  </div>
</template>

<script>
import Chart from '@/components/Chart'
export default {
  props: ['id'],
  name: 'homepage',
  components: {
    Chart
  },
  data () {
    return {
      datacollection: 0
    }
  },
  beforeMount () {
    this.fillData()
  },
  mounted () {
    // window.displayGraph()
  },
  methods: {
    fillData () {
      this.datacollection = {
        labels: ['Red', 'Green', 'Blue'],
        datasets: [{
          labels: 'Sample Dataset',
          data: [10, 20, 30],
          backgroundColor: [
            'rgba(255, 0, 0, 1)',
            'rgba(0, 255, 0, 1)',
            'rgba(0, 0, 255, 1)'
          ],
          borderColor: [
            'rgba(255,99,132,1)',
            'rgba(54, 162, 235, 1)',
            'rgba(255, 206, 86, 1)'
          ]
        }]
      }
    }
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
