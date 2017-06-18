<template>
  <div class="homepage">
    <h1>Homepage view</h1>
    <div style="width:40%">
      <Chart :chartData="datacollection"></Chart>
    </div>
    
    <canvas id="myChart"></canvas>
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
      datacollection: {}
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

</style>
